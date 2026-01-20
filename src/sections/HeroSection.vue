<script setup>
import { onMounted, ref } from "vue";
import { gsap } from "gsap";

const heroRef = ref(null);

onMounted(() => {
  const ctx = gsap.context(() => {
    // 1. Animasi Horizontal Scroll (Marquee)
    // Tetap dipertahankan karena Anda suka efek ini
    gsap.to(".marquee-text", {
      xPercent: -50,
      repeat: -1,
      duration: 20,
      ease: "linear",
    });

    // 2. Animasi Elemen Masuk (AOS Style menggunakan GSAP)
    const tl = gsap.timeline({ defaults: { ease: "power3.out" } });

    tl.from(".hero-content-anim", {
      y: 50,
      opacity: 0,
      duration: 1,
      stagger: 0.15,
    })
    .from(".hero-image-anim", {
      scale: 0.8,
      opacity: 0,
      duration: 1.2,
      ease: "back.out(1.7)",
    }, "-=0.8");

  }, heroRef.value);
});
</script>

<template>
  <section ref="heroRef" id="home" class="relative h-[100dvh] flex items-center justify-center overflow-hidden bg-primary">
    
    <div class="absolute inset-0 bg-grid-pattern opacity-20 pointer-events-none z-0"></div>
    
    <div class="absolute top-[-10%] right-[-5%] w-[500px] h-[500px] bg-secondary/10 rounded-full blur-[120px] animate-pulse-slow pointer-events-none z-0"></div>
    <div class="absolute bottom-[-10%] left-[-10%] w-[400px] h-[400px] bg-accent/10 rounded-full blur-[100px] animate-pulse-slow pointer-events-none z-0"></div>

    <div class="absolute top-1/2 -translate-y-1/2 w-full overflow-hidden opacity-5 pointer-events-none select-none z-0">
      <div class="marquee-text flex whitespace-nowrap">
        <!-- <span class="text-[10rem] lg:text-[15rem] font-display font-bold text-white leading-none px-4">
          DAKWAH CREATOR • PUBLIC SPEAKER • YOUTH INFLUENCER • 
        </span>
        <span class="text-[10rem] lg:text-[15rem] font-display font-bold text-white leading-none px-4">
          DAKWAH CREATOR • PUBLIC SPEAKER • YOUTH INFLUENCER • 
        </span> -->
      </div>
    </div>
    <div class="max-w-7xl w-full mx-auto px-6 lg:px-12 relative z-10 pt-16">
      <div class="grid lg:grid-cols-2 gap-8 lg:gap-12 items-center">
        
        <div class="text-center lg:text-left space-y-5 order-2 lg:order-1">
          
          <div class="hero-content-anim inline-flex items-center gap-2 px-3 py-1.5 rounded-full glass-panel border border-secondary/20 shadow-[0_0_15px_rgba(0,224,255,0.05)] mx-auto lg:mx-0">
            <span class="relative flex h-2 w-2">
              <span class="animate-ping absolute inline-flex h-full w-full rounded-full bg-secondary opacity-75"></span>
              <span class="relative inline-flex rounded-full h-2 w-2 bg-secondary"></span>
            </span>
            <span class="text-[10px] font-mono text-secondary tracking-widest uppercase">Dakwah & Lifestyle</span>
          </div>

          <h1 class="hero-content-anim text-4xl lg:text-6xl font-display font-bold leading-tight text-white tracking-tight">
            Merangkul Jiwa, <br />
            <span class="text-transparent bg-clip-text bg-gradient-to-r from-white via-secondary to-accent glow-text">
              Menebar Hidayah.
            </span>
          </h1>

          <p class="hero-content-anim text-slate-400 text-sm lg:text-base leading-relaxed max-w-lg mx-auto lg:mx-0">
            Hai, saya <strong class="text-white">Bintang Ramadan</strong>. Mengajak generasi muda kembali mencintai Islam dengan cara yang asik, relevan, dan menyentuh hati.
          </p>

          <div class="hero-content-anim flex flex-wrap gap-3 justify-center lg:justify-start pt-2">
            <a href="#contact" 
               class="px-6 py-3 bg-secondary text-primary font-bold text-xs uppercase tracking-widest rounded-lg hover:shadow-[0_0_20px_rgba(0,224,255,0.4)] transition-all transform hover:-translate-y-1">
              Undang Kajian
            </a>
            <a href="#portfolio" 
               class="px-6 py-3 bg-transparent border border-white/20 text-white font-bold text-xs uppercase tracking-widest rounded-lg hover:bg-white/5 transition-all">
              Lihat Konten
            </a>
          </div>

          <div class="hero-content-anim pt-4 flex items-center justify-center lg:justify-start gap-4 opacity-80">
            <div class="flex items-center gap-1.5 text-slate-400">
               <span class="material-symbols-outlined text-base">check_circle</span>
               <span class="text-[10px] font-mono uppercase">20k+ Jamaah Online</span>
            </div>
          </div>
        </div>

        <div class="hero-image-anim relative flex items-center justify-center order-1 lg:order-2">
          
          <div class="absolute w-[280px] h-[280px] lg:w-[400px] lg:h-[400px] border border-secondary/20 rounded-full animate-[spin_20s_linear_infinite]"></div>
          
          <div class="relative z-10 w-[240px] h-[320px] lg:w-[320px] lg:h-[420px] bg-surface-light rounded-2xl border border-white/10 overflow-hidden shadow-2xl group rotate-2 hover:rotate-0 transition-all duration-500">
            
            <div class="absolute inset-0 bg-gradient-to-t from-primary/80 to-transparent z-20"></div>
            
            <img 
              src="/bintang.jpeg" 
              alt="Bintang Ramadan" 
              class="w-full h-full object-cover object-top group-hover:scale-110 transition-transform duration-700"
            />

            <div class="absolute bottom-4 left-4 z-30">
               <p class="text-white font-display font-bold text-lg">Bintang Ramadan</p>
               <p class="text-secondary text-[10px] uppercase tracking-widest">Influencer Dakwah</p>
            </div>
          </div>

          <div class="absolute top-[10%] right-[10%] lg:right-[15%] glass-panel p-3 rounded-lg border border-white/10 shadow-lg animate-float z-30">
            <span class="material-symbols-outlined text-secondary text-xl">mic_external_on</span>
          </div>
        </div>

      </div>
    </div>
  </section>
</template>

<style scoped>
/* Custom Keyframes */
@keyframes float {
  0%, 100% { transform: translateY(0px); }
  50% { transform: translateY(-10px); }
}
.animate-float { animation: float 5s ease-in-out infinite; }
.animate-pulse-slow { animation: pulse 8s cubic-bezier(0.4, 0, 0.6, 1) infinite; }
</style>