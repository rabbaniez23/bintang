<script setup>
import { onMounted, ref } from "vue";
import { gsap } from "gsap";
import { ScrollTrigger } from "gsap/ScrollTrigger";

gsap.registerPlugin(ScrollTrigger);

const galleryRef = ref(null);

// Data Gambar Random (Unsplash)
const galleryImages = [
  {
    src: "https://images.unsplash.com/photo-1475721027767-p05fa6e20db7?ixlib=rb-1.2.1&auto=format&fit=crop&w=800&q=80", // Mic di panggung
    event: "Kajian Akbar Bandung",
    year: "2025",
  },
  {
    src: "https://images.unsplash.com/photo-1515168816178-541c851c597d?ixlib=rb-1.2.1&auto=format&fit=crop&w=800&q=80", // Audiens
    event: "Youth Hijrah Fest",
    year: "2025",
  },
  {
    src: "https://images.unsplash.com/photo-1560250097-0b93528c311a?ixlib=rb-1.2.1&auto=format&fit=crop&w=800&q=80", // Speaker cowok
    event: "Goes to Campus UPI",
    year: "2024",
  },
  {
    src: "https://images.unsplash.com/photo-1557804506-669a67965ba0?ixlib=rb-1.2.1&auto=format&fit=crop&w=800&q=80", // Suasana seminar
    event: "Workshop Konten Kreatif",
    year: "2024",
  },
  {
    src: "https://images.unsplash.com/photo-1519085360753-af0119f7cbe7?ixlib=rb-1.2.1&auto=format&fit=crop&w=800&q=80", // Panggung gelap
    event: "Safari Dakwah Jawa",
    year: "2023",
  },
  {
    src: "https://images.unsplash.com/photo-1544531696-60c35eb8d626?ixlib=rb-1.2.1&auto=format&fit=crop&w=800&q=80", // Crowd ramai
    event: "Meet & Greet Community",
    year: "2023",
  },
];

onMounted(() => {
  const ctx = gsap.context(() => {
    // 1. Animasi Header
    gsap.from(".gallery-header-anim", {
      scrollTrigger: {
        trigger: galleryRef.value,
        start: "top 80%",
        toggleActions: "play reverse play reverse",
      },
      y: 30,
      opacity: 0,
      duration: 1,
      ease: "power2.out",
    });

    // 2. Animasi Grid Foto (Muncul dari bawah)
    gsap.from(".gallery-item", {
      scrollTrigger: {
        trigger: ".gallery-grid",
        start: "top 75%",
        toggleActions: "play reverse play reverse",
      },
      y: 50,
      opacity: 0,
      duration: 0.8,
      stagger: 0.15,
      ease: "power2.out",
    });
  }, galleryRef.value);
});
</script>

<template>
  <section
    ref="galleryRef"
    class="py-32 bg-primary relative overflow-hidden"
    id="gallery"
  >
    <div
      class="absolute inset-0 bg-grid-pattern opacity-20 pointer-events-none z-0"
    ></div>

    <div
      class="absolute top-[-10%] right-[-5%] w-[500px] h-[500px] bg-secondary/10 rounded-full blur-[120px] animate-pulse-slow pointer-events-none z-0"
    ></div>
    <div
      class="absolute bottom-[-10%] left-[-10%] w-[400px] h-[400px] bg-accent/10 rounded-full blur-[100px] animate-pulse-slow pointer-events-none z-0"
    ></div>
    <div
      class="max-w-7xl mx-auto px-6 lg:px-8 mb-16 text-center gallery-header-anim relative z-10"
    >
      <span
        class="text-secondary font-display font-bold tracking-[0.2em] uppercase text-sm mb-4 block"
      >
        // Dokumentasi Kegiatan
      </span>
      <h2
        class="text-4xl md:text-6xl font-display font-bold text-white mb-6 tracking-tight"
      >
        REKAM JEJAK
        <span
          class="text-transparent bg-clip-text bg-gradient-to-r from-secondary to-accent"
          >KEBAIKAN</span
        >
      </h2>
      <p
        class="text-slate-400 max-w-2xl mx-auto text-lg font-light leading-relaxed"
      >
        Setiap pertemuan adalah kesempatan untuk saling mengingatkan. Berikut
        adalah dokumentasi perjalanan dakwah dan kolaborasi di berbagai kota.
      </p>
    </div>

    <div class="max-w-7xl mx-auto px-6 lg:px-8 relative z-10">
      <div
        class="gallery-grid columns-1 md:columns-2 lg:columns-3 gap-6 space-y-6"
      >
        <div
          v-for="(item, index) in galleryImages"
          :key="index"
          class="gallery-item break-inside-avoid relative group rounded-2xl overflow-hidden shadow-2xl border border-white/5 bg-surface-light"
        >
          <img
            :src="item.src"
            :alt="item.event"
            class="w-full h-auto object-cover transform group-hover:scale-105 transition-transform duration-700 grayscale group-hover:grayscale-0"
          />

          <div
            class="absolute inset-0 bg-gradient-to-t from-primary/90 via-primary/20 to-transparent opacity-0 group-hover:opacity-100 transition-opacity duration-300 flex flex-col justify-end p-6"
          >
            <span class="text-secondary text-xs font-mono mb-1">{{
              item.year
            }}</span>
            <h3
              class="text-white font-display font-bold uppercase tracking-wider text-lg"
            >
              {{ item.event }}
            </h3>
          </div>

          <div
            class="absolute top-4 right-4 w-2 h-2 bg-secondary rounded-full opacity-0 group-hover:opacity-100 transition-opacity duration-500 shadow-[0_0_10px_#00e0ff]"
          ></div>
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped>
.animate-pulse-slow {
  animation: pulse 8s cubic-bezier(0.4, 0, 0.6, 1) infinite;
}

@keyframes pulse {
  0%,
  100% {
    opacity: 1;
  }
  50% {
    opacity: 0.5;
  }
}
</style>
