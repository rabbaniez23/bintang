<script setup>
import { onMounted, ref } from "vue";
import { gsap } from "gsap";
import { ScrollTrigger } from "gsap/ScrollTrigger";

gsap.registerPlugin(ScrollTrigger);

const eduSection = ref(null);

const education = [
  {
    year: "2010 - 2016",
    school: "SDIT Al-Amanah",
    major: "Pendidikan Dasar",
    desc: "Membangun fondasi karakter islami dan kecintaan pada ilmu pengetahuan sejak dini.",
    icon: "backpack",
  },
  {
    year: "2016 - 2019",
    school: "SMP IT Insan Cendekia",
    major: "Junior High School",
    desc: "Aktif dalam organisasi OSIS dan mulai mendalami public speaking melalui kegiatan muhadharah.",
    icon: "menu_book",
  },
  {
    year: "2019 - 2022",
    school: "SMA Negeri 3 Bandung",
    major: "Jurusan IPA",
    desc: "Fokus pada akademik sains sambil aktif memimpin Rohis (Rohani Islam) sekolah.",
    icon: "science",
  },
  {
    year: "2022 - 2025",
    school: "Pondok Pesantren Al-Musaddadiyah",
    major: "Tafaqquh Fiddin",
    desc: "Mendalami ilmu agama, kitab kuning, dan pembentukan akhlak sebelum terjun ke dunia kampus.",
    icon: "mosque",
  },
  {
    year: "2025 - Sekarang",
    school: "Universitas Pendidikan Indonesia",
    major: "S1 Ilmu Komputer",
    desc: "Mahasiswa aktif Kelas C2. Menggabungkan teknologi (AI/Web) dengan dakwah digital.",
    icon: "computer",
  },
];

onMounted(() => {
  const ctx = gsap.context(() => {
    // Animasi Judul
    gsap.from(".edu-header-anim", {
      scrollTrigger: {
        trigger: eduSection.value,
        start: "top 80%",
        toggleActions: "play reverse play reverse",
      },
      y: 30,
      opacity: 0,
      duration: 1,
      ease: "power2.out",
    });

    // Animasi Timeline Item
    // Kita pakai .from() simpel agar item muncul dari kiri/kanan mendekati garis tengah
    education.forEach((_, i) => {
      const direction = i % 2 === 0 ? -50 : 50; // Genap dari kiri, Ganjil dari kanan

      gsap.from(`.timeline-item-${i}`, {
        scrollTrigger: {
          trigger: `.timeline-item-${i}`,
          start: "top 85%",
          toggleActions: "play reverse play reverse",
        },
        x: direction,
        opacity: 0,
        duration: 1,
        ease: "power3.out",
      });

      // Animasi Titik Tengah (Dot)
      gsap.from(`.timeline-dot-${i}`, {
        scrollTrigger: {
          trigger: `.timeline-item-${i}`,
          start: "top 85%",
          toggleActions: "play reverse play reverse",
        },
        scale: 0,
        opacity: 0,
        duration: 0.5,
        delay: 0.3,
        ease: "back.out(2)",
      });
    });
  }, eduSection.value);
});
</script>

<template>
  <section
    ref="eduSection"
    class="relative py-32 bg-primary overflow-hidden"
    id="expertise"
  >
    <div
      class="absolute inset-0 bg-grid-pattern opacity-20 pointer-events-none"
    ></div>
    <div
      class="absolute top-[20%] right-[-10%] w-[500px] h-[500px] bg-secondary/10 rounded-full blur-[120px] animate-pulse-slow pointer-events-none"
    ></div>
    <div
      class="absolute bottom-[-10%] left-[-10%] w-[400px] h-[400px] bg-accent/10 rounded-full blur-[100px] animate-pulse-slow pointer-events-none"
    ></div>
    <div class="max-w-7xl mx-auto px-6 lg:px-8 relative z-10">
      <div class="text-center mb-24 edu-header-anim">
        <span
          class="text-secondary font-display font-bold tracking-[0.2em] uppercase text-sm mb-4 block"
        >
          // Academic Journey
        </span>
        <h2
          class="text-4xl md:text-6xl font-display font-bold text-white tracking-tight"
        >
          JEJAK
          <span
            class="text-transparent bg-clip-text bg-gradient-to-r from-secondary to-accent"
            >PENDIDIKAN</span
          >
        </h2>
      </div>

      <div class="relative wrap overflow-hidden p-4 md:p-0">
        <div
          class="absolute border-opacity-20 border-white/20 h-full border-l-2 left-8 md:left-1/2 top-0 transform md:-translate-x-1/2"
        ></div>

        <div
          v-for="(edu, index) in education"
          :key="index"
          :class="`timeline-item-${index} mb-12 flex justify-between items-center w-full ${index % 2 === 0 ? 'flex-row-reverse md:flex-row-reverse' : 'flex-row-reverse md:flex-row'}`"
        >
          <div class="hidden md:block w-5/12"></div>

          <div
            :class="`timeline-dot-${index} z-20 flex items-center order-1 bg-surface shadow-xl w-12 h-12 rounded-full border-2 border-secondary relative left-[14px] md:left-0`"
          >
            <h1 class="mx-auto font-semibold text-lg text-white">
              <span class="material-symbols-outlined text-sm text-secondary">{{
                edu.icon
              }}</span>
            </h1>
          </div>

          <div class="order-1 w-full md:w-5/12 pl-12 md:pl-0">
            <div
              class="bg-surface-light border border-white/5 p-6 rounded-xl hover:border-secondary/30 transition-all duration-300 hover:shadow-neon/10 group relative"
            >
              <div
                v-if="index % 2 !== 0"
                class="hidden md:block absolute top-6 -left-2 w-4 h-4 bg-surface-light border-l border-b border-white/5 transform rotate-45"
              ></div>
              <div
                v-else
                class="hidden md:block absolute top-6 -right-2 w-4 h-4 bg-surface-light border-r border-t border-white/5 transform rotate-45"
              ></div>

              <span
                class="mb-2 inline-block px-3 py-1 rounded-full bg-white/5 border border-white/10 text-[10px] font-mono text-secondary"
              >
                {{ edu.year }}
              </span>
              <h3
                class="font-display font-bold text-xl text-white mb-1 group-hover:text-secondary transition-colors"
              >
                {{ edu.school }}
              </h3>
              <p class="text-white/70 text-sm font-medium mb-3">
                {{ edu.major }}
              </p>
              <p class="text-slate-400 text-sm font-light leading-relaxed">
                {{ edu.desc }}
              </p>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>
