<script setup>
import { onMounted, ref } from "vue";
import { gsap } from "gsap";
import { ScrollTrigger } from "gsap/ScrollTrigger";

gsap.registerPlugin(ScrollTrigger);

const aboutSection = ref(null);

// Data Skill dengan Ikon & Deskripsi
const skills = [
  {
    title: "Public Speaking",
    desc: "Retorika yang menyentuh hati & persuasif.",
    icon: "record_voice_over"
  },
  {
    title: "Digital Dakwah",
    desc: "Konten kreatif yang relevan untuk Gen-Z.",
    icon: "play_circle"
  },
  {
    title: "Youth Psychology",
    desc: "Pendekatan personal memahami keresahan anak muda.",
    icon: "psychology"
  },
  {
    title: "Community Building",
    desc: "Menggerakkan komunitas hijrah yang suportif.",
    icon: "diversity_3"
  }
];

onMounted(() => {
  const ctx = gsap.context(() => {
    // 1. Animasi Teks (Kiri)
    gsap.from(".about-content-anim", {
      scrollTrigger: {
        trigger: aboutSection.value,
        start: "top 80%",
      },
      x: -50,
      opacity: 0,
      duration: 1,
      stagger: 0.15,
      ease: "power3.out"
    });

    // 2. Animasi Kartu (Kanan) - Muncul satu per satu
    gsap.from(".skill-card-anim", {
      scrollTrigger: {
        trigger: ".skills-grid",
        start: "top 85%",
      },
      y: 40,
      opacity: 0,
      duration: 0.8,
      stagger: 0.1, // Jeda antar kartu
      ease: "back.out(1.5)" // Efek membal sedikit
    });
  }, aboutSection.value);
});
</script>

<template>
  <section
    ref="aboutSection"
    class="py-24 relative bg-surface overflow-hidden"
    id="about"
  >
    <div class="absolute top-0 left-0 w-1/3 h-full bg-gradient-to-r from-primary/50 to-transparent pointer-events-none"></div>
    <div class="absolute bottom-[-100px] right-[-100px] w-[500px] h-[500px] bg-secondary/5 rounded-full blur-[120px] pointer-events-none"></div>

    <div class="max-w-7xl mx-auto px-6 lg:px-8 relative z-10">
      <div class="grid lg:grid-cols-2 gap-16 lg:gap-24 items-center">
        
        <div class="space-y-8">
          <div class="about-content-anim inline-flex items-center gap-2 px-3 py-1 rounded-full bg-white/5 border border-white/10 w-fit">
            <span class="w-2 h-2 rounded-full bg-secondary animate-pulse"></span>
            <span class="text-[10px] text-secondary uppercase tracking-widest font-bold">Tentang Bintang</span>
          </div>

          <h2 class="about-content-anim text-4xl lg:text-5xl font-display font-bold text-white leading-tight">
            Lebih Dari Sekadar <br />
            <span class="text-transparent bg-clip-text bg-gradient-to-r from-secondary to-accent">Kata-Kata.</span>
          </h2>

          <div class="about-content-anim space-y-6 text-slate-400 text-lg leading-relaxed font-light">
            <p>
              Assalamualaikum! Perjalanan saya bukan tentang menjadi yang paling benar, tapi tentang mengajak teman-teman melangkah bersama ke arah yang lebih baik.
            </p>
            <p>
              Saya melihat banyak anak muda yang sebenarnya rindu pada agama, tapi merasa "terhakimi" oleh penyampaian yang kaku. Di sinilah saya hadir.
            </p>
            <p>
              Dengan bekal 
              <strong class="text-white font-normal">Public Speaking</strong> dan 
              <strong class="text-white font-normal">Content Creation</strong>, 
              saya mengemas pesan dakwah menjadi sesuatu yang asik, estetik, dan mudah diterima logika maupun hati generasi Z.
            </p>
          </div>

          <div class="about-content-anim pt-4 border-l-4 border-secondary/30 pl-6">
            <p class="text-white italic font-display text-xl">"Dakwah is Art. Make it beautiful."</p>
            <p class="text-sm text-slate-500 mt-2 uppercase tracking-widest">— Bintang Ramadan</p>
          </div>
        </div>

        <div class="skills-grid grid grid-cols-1 sm:grid-cols-2 gap-6">
          
          <div 
            v-for="(skill, index) in skills" 
            :key="index"
            class="skill-card-anim group relative p-6 bg-surface-light rounded-2xl border border-white/5 hover:border-secondary/30 transition-all duration-300 hover:-translate-y-2 hover:shadow-neon/20 cursor-default"
          >
            <div class="absolute inset-0 bg-gradient-to-br from-secondary/5 to-transparent opacity-0 group-hover:opacity-100 transition-opacity duration-500 rounded-2xl"></div>

            <div class="relative w-12 h-12 mb-6 rounded-xl bg-primary border border-white/10 flex items-center justify-center group-hover:scale-110 transition-transform duration-300 group-hover:border-secondary/50">
              <span class="material-symbols-outlined text-2xl text-slate-400 group-hover:text-secondary transition-colors duration-300">
                {{ skill.icon }}
              </span>
            </div>

            <h3 class="relative text-xl font-display font-bold text-white mb-2 group-hover:text-secondary transition-colors">
              {{ skill.title }}
            </h3>
            
            <p class="relative text-sm text-slate-400 leading-relaxed group-hover:text-slate-300 transition-colors">
              {{ skill.desc }}
            </p>
          </div>

        </div>

      </div>
    </div>
  </section>
</template>