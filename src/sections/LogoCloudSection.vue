<script setup>
import { onMounted, ref } from "vue";
import { gsap } from "gsap";
import { ScrollTrigger } from "gsap/ScrollTrigger";

gsap.registerPlugin(ScrollTrigger);

const logoSection = ref(null);

// Data Partner/Komunitas (Gunakan Teks sebagai pengganti logo SVG sementara)
// Pilih nama-nama yang relevan dengan niche Dakwah, Edukasi, dan Lifestyle Islami
const partners = [
  "KAHF EVERYDAY",
  "WARDAH BEAUTY",
  "HIJRAHFEST",
  "YUKNGAJI",
  "DOMPET DHUAFA",
  "RABBANI",
  "ISLAM ITU INDAH",
  "UPI BANDUNG",
  "KAHF EVERYDAY",
  "WARDAH BEAUTY",
  "HIJRAHFEST",
  "YUKNGAJI", // Duplikasi untuk looping
];

onMounted(() => {
  const ctx = gsap.context(() => {
    // Animasi Judul
    gsap.from(".logo-header-anim", {
      scrollTrigger: {
        trigger: logoSection.value,
        start: "top 90%",
        toggleActions: "play reverse play reverse",
      },
      y: 20,
      opacity: 0,
      duration: 1,
      ease: "power2.out",
    });
    // Animasi Marquee (Muncul pelan)
    gsap.from(".logo-marquee-anim", {
      scrollTrigger: {
        trigger: logoSection.value,
        start: "top 85%",
        toggleActions: "play reverse play reverse",
      },
      opacity: 0,
      duration: 1.5,
      delay: 0.3,
      ease: "power2.out",
    });
  }, logoSection.value);
});
</script>

<template>
  <section ref="logoSection" class="py-24 bg-primary relative overflow-hidden">
    <div
      class="absolute inset-0 bg-grid-pattern opacity-20 pointer-events-none"
    ></div>
    <div
      class="absolute top-[-20%] left-[30%] w-[600px] h-[600px] bg-secondary/5 rounded-full blur-[150px] animate-pulse-slow pointer-events-none"
    ></div>
    <div class="max-w-7xl mx-auto px-6 lg:px-8 text-center relative z-10">
      <p
        class="logo-header-anim text-secondary text-xs font-display font-bold uppercase tracking-[0.3em] mb-12"
      >
        // Dipercaya Oleh Komunitas & Brand
      </p>

      <div
        class="relative w-full overflow-hidden mask-gradient py-6 logo-marquee-anim"
      >
        <div
          class="flex gap-16 md:gap-24 items-center whitespace-nowrap animate-marquee w-max"
        >
          <div
            v-for="(partner, index) in partners"
            :key="index"
            class="text-xl md:text-2xl font-display font-bold text-white/30 hover:text-secondary transition-colors cursor-default uppercase tracking-wider"
          >
            {{ partner }}
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped>
/* Mask Gradient untuk efek fade di kiri-kanan */
.mask-gradient {
  mask-image: linear-gradient(
    to right,
    transparent,
    black 15%,
    black 85%,
    transparent
  );
  -webkit-mask-image: linear-gradient(
    to right,
    transparent,
    black 15%,
    black 85%,
    transparent
  );
}

/* Animasi Marquee */
.animate-marquee {
  animation: marquee 40s linear infinite; /* Kecepatan disesuaikan agar tidak terlalu cepat */
}

@keyframes marquee {
  0% {
    transform: translateX(0);
  }
  100% {
    transform: translateX(-50%);
  } /* Geser 50% karena kita menduplikasi array */
}

/* Animasi Pulse untuk Orbs */
.animate-pulse-slow {
  animation: pulse 10s cubic-bezier(0.4, 0, 0.6, 1) infinite;
}

@keyframes pulse {
  0%,
  100% {
    opacity: 1;
  }
  50% {
    opacity: 0.6;
  }
}
</style>
