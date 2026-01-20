<script setup>
import { onMounted, ref } from "vue";
import { gsap } from "gsap";
import { ScrollTrigger } from "gsap/ScrollTrigger";

gsap.registerPlugin(ScrollTrigger);

const portfolioRef = ref(null);

// Data Portofolio: Kombinasi Dakwah, Tech (CS Student), dan Event
const projects = ref([
  {
    category: "Community Platform",
    title: "Hijrah Creative Hub",
    desc: "Wadah kolaborasi bagi konten kreator muslim untuk menciptakan narasi positif di media sosial.",
    image:
      "https://images.unsplash.com/photo-1531482615713-2afd69097998?ixlib=rb-1.2.1&auto=format&fit=crop&w=800&q=80",
    year: "2025",
  },
  {
    category: "Digital Content",
    title: "Podcast 'Ngopi Iman'",
    desc: "Serial podcast mingguan yang membahas isu anak muda dari sudut pandang Islam yang santai.",
    image:
      "https://images.unsplash.com/photo-1478737270239-2f02b77ac618?ixlib=rb-1.2.1&auto=format&fit=crop&w=800&q=80",
    year: "2024",
  },
  {
    category: "Web Development",
    title: "Aplikasi 'MasjidKu'",
    desc: "Sistem manajemen masjid berbasis web untuk memudahkan infaq dan jadwal kajian (Skripsi Project).",
    image:
      "https://images.unsplash.com/photo-1555066931-4365d14bab8c?ixlib=rb-1.2.1&auto=format&fit=crop&w=800&q=80",
    year: "2024",
  },
  {
    category: "Event Organizer",
    title: "Youth Leadership Camp",
    desc: "Bootcamp kepemimpinan islam selama 3 hari untuk mencetak pemimpin masa depan berkarakter.",
    image:
      "https://images.unsplash.com/photo-1517245386807-bb43f82c33c4?ixlib=rb-1.2.1&auto=format&fit=crop&w=800&q=80",
    year: "2023",
  },
  {
    category: "Publication",
    title: "Buku 'Jalan Pulang'",
    desc: "Buku antologi kisah inspiratif perjalanan hijrah generasi milenial (Best Seller Lokal).",
    image:
      "https://images.unsplash.com/photo-1544947950-fa07a98d237f?ixlib=rb-1.2.1&auto=format&fit=crop&w=800&q=80",
    year: "2023",
  },
  {
    category: "Education",
    title: "Mentoring Beasiswa",
    desc: "Program bimbingan intensif untuk pelajar yang ingin melanjutkan studi ke Timur Tengah & Eropa.",
    image:
      "https://images.unsplash.com/photo-1523240795612-9a054b0db644?ixlib=rb-1.2.1&auto=format&fit=crop&w=800&q=80",
    year: "2022",
  },
]);

onMounted(() => {
  const ctx = gsap.context(() => {
    // 1. Animasi Header
    gsap.from(".port-header-anim", {
      scrollTrigger: {
        trigger: portfolioRef.value,
        start: "top 80%",
        toggleActions: "play reverse play reverse",
      },
      y: 30,
      opacity: 0,
      duration: 1,
      ease: "power2.out",
    });

    // 2. Animasi Kartu Portofolio
    gsap.fromTo(
      ".port-card-anim",
      { y: 50, autoAlpha: 0 },
      {
        y: 0,
        autoAlpha: 1,
        duration: 0.8,
        stagger: 0.1,
        ease: "power2.out",
        scrollTrigger: {
          trigger: ".portfolio-grid",
          start: "top bottom",
          toggleActions: "play reverse play reverse",
        },
      },
    );
  }, portfolioRef.value);
});
</script>

<template>
  <section
    ref="portfolioRef"
    class="py-32 bg-primary relative overflow-hidden"
    id="portfolio"
  >
    <div
      class="absolute inset-0 bg-grid-pattern opacity-20 pointer-events-none"
    ></div>
    <div
      class="absolute top-[20%] right-[-10%] w-[600px] h-[600px] bg-secondary/10 rounded-full blur-[120px] animate-pulse-slow pointer-events-none"
    ></div>
    <div
      class="absolute bottom-[-10%] left-[-10%] w-[500px] h-[500px] bg-accent/10 rounded-full blur-[100px] animate-pulse-slow pointer-events-none"
    ></div>
    <div class="max-w-7xl mx-auto px-6 lg:px-8 relative z-10">
      <div
        class="flex flex-col md:flex-row justify-between items-end mb-16 gap-6 border-b border-white/10 pb-8 port-header-anim"
      >
        <div>
          <span
            class="text-secondary font-display font-bold tracking-[0.2em] uppercase text-sm mb-2 block"
          >
            // Featured Works
          </span>
          <h2 class="text-4xl md:text-5xl font-display font-bold text-white">
            KARYA &
            <span
              class="text-transparent bg-clip-text bg-gradient-to-r from-secondary to-accent"
              >KONTRIBUSI</span
            >
          </h2>
        </div>
        <p
          class="text-slate-400 max-w-sm text-sm text-right md:text-left font-light"
        >
          Kumpulan inisiatif, proyek digital, dan gerakan sosial yang telah saya
          bangun untuk umat.
        </p>
      </div>

      <div
        class="portfolio-grid grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8"
      >
        <div
          v-for="(project, index) in projects"
          :key="index"
          class="port-card-anim group relative rounded-2xl overflow-hidden border border-white/10 bg-surface-light shadow-2xl hover:border-secondary/30 transition-all duration-500 hover:-translate-y-2 hover:shadow-neon/20"
        >
          <div class="h-48 w-full overflow-hidden relative">
            <!-- Removed opacity overlay for better visibility -->
            <img
              :src="project.image"
              :alt="project.title"
              class="w-full h-full object-cover transform group-hover:scale-110 transition-transform duration-700"
            />
          </div>

          <div class="p-6 relative">
            <div
              class="absolute inset-0 bg-gradient-to-b from-transparent to-secondary/5 opacity-0 group-hover:opacity-100 transition-opacity duration-500"
            ></div>

            <div class="relative z-10">
              <div class="flex justify-between items-center mb-3">
                <span
                  class="text-[10px] font-mono uppercase tracking-widest text-secondary bg-secondary/10 px-2 py-1 rounded border border-secondary/20"
                >
                  {{ project.category }}
                </span>
                <span class="text-slate-500 text-xs font-mono">{{
                  project.year
                }}</span>
              </div>

              <h3
                class="text-xl font-display font-bold text-white mb-2 group-hover:text-secondary transition-colors"
              >
                {{ project.title }}
              </h3>

              <p
                class="text-sm text-slate-400 font-light leading-relaxed line-clamp-3 group-hover:text-slate-300 transition-colors"
              >
                {{ project.desc }}
              </p>

              <div
                class="mt-4 flex items-center gap-2 text-secondary text-xs font-bold uppercase tracking-widest opacity-0 group-hover:opacity-100 transform translate-y-2 group-hover:translate-y-0 transition-all duration-300"
              >
                Lihat Detail
                <span class="material-symbols-outlined text-sm"
                  >arrow_forward</span
                >
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>
