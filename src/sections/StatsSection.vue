<script setup>
import { onMounted, ref } from "vue";
import { gsap } from "gsap";
import { ScrollTrigger } from "gsap/ScrollTrigger";

gsap.registerPlugin(ScrollTrigger);

const sectionRef = ref(null);

// Data Skill: Disesuaikan untuk Influencer Dakwah
const skills = [
  { 
    name: "Public Speaking & Dakwah", 
    percent: 95, 
    icon: "podium", // Ikon panggung/ceramah
    desc: "Menyampaikan nilai Islam dengan bahasa yang renyah & relevan." 
  },
  { 
    name: "Digital Content Creation", 
    percent: 90, 
    icon: "video_camera_front", // Ikon konten kreator
    desc: "Mengemas pesan kebaikan dalam format visual yang estetik."
  },
  { 
    name: "Youth Engagement", 
    percent: 92, 
    icon: "diversity_2", // Ikon anak muda/komunitas
    desc: "Pendekatan personal yang 'relate' dengan masalah Gen-Z."
  },
  { 
    name: "Community Building", 
    percent: 88, 
    icon: "hub", // Ikon jaringan/ukhuwah
    desc: "Membangun ekosistem hijrah yang suportif & asik."
  },
];

onMounted(() => {
  const ctx = gsap.context(() => {
    // 1. Animasi Teks Muncul
    gsap.from(".skill-text", {
      scrollTrigger: {
        trigger: sectionRef.value,
        start: "top 80%",
      },
      y: 30,
      opacity: 0,
      duration: 0.8,
      stagger: 0.1,
      ease: "power2.out"
    });

    // 2. Animasi Bar (Width 0 -> Target)
    skills.forEach((skill, index) => {
      gsap.fromTo(`.bar-fill-${index}`, 
        { width: "0%" },
        {
          width: `${skill.percent}%`,
          duration: 1.5,
          ease: "power2.out",
          scrollTrigger: {
            trigger: sectionRef.value,
            start: "top 75%",
          }
        }
      );
      
      // Animasi Angka (Counter)
      gsap.fromTo(`.counter-${index}`,
        { innerText: 0 },
        {
          innerText: skill.percent,
          duration: 1.5,
          snap: { innerText: 1 },
          scrollTrigger: {
            trigger: sectionRef.value,
            start: "top 75%",
          }
        }
      );
    });
  }, sectionRef.value);
});
</script>

<template>
  <section
    ref="sectionRef"
    class="relative py-24 bg-surface border-y border-white/5 overflow-hidden"
  >
    <div class="absolute inset-0 bg-grid-pattern opacity-10 pointer-events-none"></div>
    <div class="absolute -right-20 bottom-0 w-64 h-64 bg-secondary/10 rounded-full blur-[120px]"></div>

    <div class="max-w-7xl mx-auto px-6 lg:px-12 relative z-10">
      <div class="grid lg:grid-cols-2 gap-16 items-center">
        
        <div class="skill-text space-y-6">
          <div class="inline-flex items-center gap-2 px-3 py-1 rounded-full border border-secondary/30 bg-secondary/5 text-secondary text-xs font-mono uppercase tracking-widest">
            <span class="w-2 h-2 rounded-full bg-secondary animate-pulse"></span>
            Impact & Reach
          </div>
          
          <h2 class="text-4xl lg:text-5xl font-display font-bold text-white leading-tight">
            Menyebarkan Kebaikan <br />
            <span class="text-transparent bg-clip-text bg-gradient-to-r from-secondary to-accent">Di Era Digital.</span>
          </h2>
          
          <p class="text-slate-400 text-lg leading-relaxed">
            Dakwah hari ini bukan sekadar ceramah di atas mimbar, tapi bagaimana pesan itu sampai ke 
            <strong class="text-white">beranda media sosial</strong> dan 
            <strong class="text-white">hati generasi muda</strong>. 
            Saya menggabungkan nilai Islam dengan kreativitas visual.
          </p>

          <div class="pt-6 flex gap-8 border-t border-white/10 mt-8">
            <div>
              <p class="text-3xl font-display font-bold text-white">20k+</p>
              <p class="text-xs text-slate-500 uppercase tracking-widest mt-1">Instagram Followers</p>
            </div>
            <div>
              <p class="text-3xl font-display font-bold text-white">100+</p>
              <p class="text-xs text-slate-500 uppercase tracking-widest mt-1">Kajian Offline</p>
            </div>
            <div>
              <p class="text-3xl font-display font-bold text-white">1M+</p>
              <p class="text-xs text-slate-500 uppercase tracking-widest mt-1">Total Views</p>
            </div>
          </div>
        </div>

        <div class="space-y-8">
          <div 
            v-for="(skill, index) in skills" 
            :key="index"
            class="skill-text group"
          >
            <div class="flex justify-between items-end mb-2">
              <div class="flex items-center gap-3">
                <span class="material-symbols-outlined text-secondary/80 text-xl">{{ skill.icon }}</span>
                <div>
                  <h4 class="text-white font-bold font-display tracking-wide">{{ skill.name }}</h4>
                  <p class="text-[10px] text-slate-500 uppercase tracking-wider hidden sm:block">{{ skill.desc }}</p>
                </div>
              </div>
              <div class="text-right">
                <span class="text-xl font-mono font-bold text-secondary counter-{{ index }}">0</span>
                <span class="text-secondary text-sm">%</span>
              </div>
            </div>

            <div class="h-3 w-full bg-surface-light rounded-full overflow-hidden border border-white/5 relative">
              <div 
                :class="`bar-fill-${index} absolute top-0 left-0 h-full bg-gradient-to-r from-secondary to-accent rounded-full shadow-[0_0_15px_rgba(0,224,255,0.6)]`"
                style="width: 0%"
              >
                <div class="absolute right-0 top-0 bottom-0 w-[2px] bg-white shadow-[0_0_10px_white]"></div>
              </div>
            </div>
          </div>
        </div>

      </div>
    </div>
  </section>
</template>