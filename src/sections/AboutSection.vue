<script setup>
import { onMounted, ref } from "vue";
import { gsap } from "gsap";
import { ScrollTrigger } from "gsap/ScrollTrigger";

gsap.registerPlugin(ScrollTrigger);

const aboutSection = ref(null);

onMounted(() => {
  gsap.from(".about-stat", {
    scrollTrigger: {
      trigger: aboutSection.value,
      start: "top 70%",
    },
    y: 30,
    opacity: 0,
    stagger: 0.1,
    duration: 0.8,
  });
});
</script>

<template>
  <section
    ref="aboutSection"
    class="py-32 relative bg-surface overflow-hidden"
    id="about"
  >
    <div
      class="absolute top-0 right-0 w-1/3 h-full bg-linear-to-l from-primary to-transparent opacity-50"
    ></div>

    <div class="max-w-7xl mx-auto px-6 lg:px-8 relative z-10">
      <div class="grid lg:grid-cols-12 gap-16 items-start">
        <!-- Profile Image Left -->
        <div class="lg:col-span-5 relative">
          <div class="relative z-10">
            <img
              src="https://images.unsplash.com/photo-1543269865-cbf427effbad?ixlib=rb-1.2.1&auto=format&fit=crop&w=800&q=80"
              alt="Profile"
              class="w-full rounded-sm grayscale hover:grayscale-0 transition-all duration-500 shadow-2xl border-2 border-white/5"
            />
            <div
              class="absolute -bottom-6 -right-6 w-32 h-32 bg-secondary/10 backdrop-blur-md border border-secondary/30 flex items-center justify-center"
            >
              <span
                class="material-symbols-outlined text-4xl text-secondary animate-pulse"
                >verified</span
              >
            </div>
          </div>
          <!-- Corner Decors -->
          <div
            class="absolute -top-4 -left-4 w-24 h-24 border-t-2 border-l-2 border-secondary"
          ></div>
          <div
            class="absolute -bottom-4 -right-4 w-24 h-24 border-b-2 border-r-2 border-secondary"
          ></div>
        </div>

        <!-- Text Content Right -->
        <div class="lg:col-span-7">
          <h2 class="text-5xl font-display font-bold text-white mb-8">
            MERANCANG <span class="text-secondary">PERUBAHAN</span>
          </h2>

          <div
            class="space-y-6 text-slate-400 font-light text-lg leading-relaxed"
          >
            <p>
              Halo! Saya Bintang. Latar belakang saya adalah perpaduan unik
              antara <strong>Teknologi Informasi</strong> dan
              <strong>Strategi Bisnis</strong>. Saya percaya bahwa teknologi
              bukan hanya alat, tapi katalisator untuk perubahan positif.
              <strong class="text-white font-normal"
                >Misi saya adalah menjembatani kesenjangan antara inovasi teknis
                dan pemahaman manusia.</strong
              >
            </p>
            <p>
              Sebagai lulusan Teknik Informatika yang kini aktif berbicara di
              berbagai forum nasional, saya menggabungkan wawasan teknis
              mendalam dengan penyampaian yang mudah dicerna. Dari ruang kelas
              universitas hingga ruang rapat direksi, saya hadir untuk membantu
              Anda memahami "what's next".
            </p>
          </div>

          <div
            class="grid grid-cols-2 md:grid-cols-4 gap-8 mt-12 pt-12 border-t border-white/10"
          >
            <div class="about-stat">
              <span
                class="block text-3xl font-display font-bold text-white mb-2"
                >15+</span
              >
              <span class="text-xs uppercase tracking-widest text-slate-500"
                >Tahun Exp</span
              >
            </div>
            <div class="about-stat">
              <span
                class="block text-3xl font-display font-bold text-white mb-2"
                >30+</span
              >
              <span class="text-xs uppercase tracking-widest text-slate-500"
                >Negara</span
              >
            </div>
            <div class="about-stat">
              <span
                class="block text-3xl font-display font-bold text-white mb-2"
                >100+</span
              >
              <span class="text-xs uppercase tracking-widest text-slate-500"
                >Klien</span
              >
            </div>
            <div class="about-stat">
              <span
                class="block text-3xl font-display font-bold text-white mb-2"
                >4.9</span
              >
              <span class="text-xs uppercase tracking-widest text-slate-500"
                >Rating</span
              >
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>
