<script setup>
import { onMounted, ref } from "vue";
import { gsap } from "gsap";

const heroRef = ref(null);

onMounted(() => {
  // GSAP animations
  const tl = gsap.timeline();

  tl.from(".hero-text-element", {
    y: 50,
    opacity: 0,
    duration: 1,
    stagger: 0.2,
    ease: "power3.out",
  });

  // Stagger the 4 images
  tl.from(
    ".hero-grid-image",
    {
      scale: 0.8,
      opacity: 0,
      duration: 0.8,
      stagger: 0.1,
      ease: "back.out(1.7)",
    },
    "-=0.5",
  );
});
</script>

<template>
  <section
    ref="heroRef"
    class="relative min-h-screen flex items-center justify-center pt-24 overflow-hidden"
    id="home"
  >
    <!-- Background Elements -->
    <div class="absolute inset-0 z-0">
      <div class="absolute inset-0 bg-primary opacity-90"></div>
      <div
        class="absolute w-[800px] h-[800px] bg-secondary/10 rounded-full blur-[120px] -top-20 -right-20 animate-pulse"
      ></div>
      <div
        class="absolute w-[600px] h-[600px] bg-accent/10 rounded-full blur-[100px] bottom-0 left-0"
      ></div>
    </div>

    <div
      class="relative z-10 max-w-7xl mx-auto px-6 lg:px-8 w-full grid lg:grid-cols-2 gap-12 items-center"
    >
      <!-- Left Content -->
      <div>
        <div class="flex items-center gap-4 mb-6 hero-text-element">
          <span class="h-px w-12 bg-secondary"></span>
          <span
            class="text-secondary font-display font-medium tracking-[0.2em] uppercase text-sm"
          >
            // Izinkan Saya Memperkenalkan Diri
          </span>
        </div>

        <h1
          class="hero-text-element text-4xl lg:text-6xl font-display font-bold text-white leading-none mb-8 tracking-tighter"
        >
          HELPING YOU <br />
          <span
            class="text-transparent bg-clip-text bg-linear-to-r from-white to-slate-500"
            >NAVIGATE THE</span
          >
          <br />
          <span class="text-secondary glow-text">FUTURE OF TECH</span>
        </h1>

        <p
          class="hero-text-element text-slate-400 text-lg lg:text-xl max-w-xl leading-relaxed mb-10 font-light border-l border-white/10 pl-6"
        >
          Seorang Tech Evangelist dan Edukator yang berfokus membantu Anda
          menemukan peluang di era kecerdasan buatan dan transformasi digital.
        </p>

        <div class="hero-text-element flex flex-wrap gap-6 items-center">
          <a
            class="bg-secondary text-primary px-8 py-4 font-display font-bold uppercase tracking-widest hover:shadow-neon hover:scale-105 transition-all duration-3000 flex items-center gap-2"
            href="/cv.pdf"
            download
          >
            <span class="material-symbols-outlined text-lg">download</span>
            Download CV
          </a>
          <a
            class="flex items-center gap-3 text-white hover:text-secondary transition-colors group"
            href="#portfolio"
          >
            <div
              class="w-12 h-12 rounded-full border border-white/20 flex items-center justify-center group-hover:border-secondary group-hover:shadow-neon transition-all"
            >
              <span class="material-symbols-outlined">visibility</span>
            </div>
            <span class="font-display uppercase tracking-widest text-xs"
              >Aktivitas Saya</span
            >
          </a>
        </div>
      </div>

      <!-- Right: 4-Grid Images -->
      <div class="relative flex items-center justify-center">
        <!-- Decorative background for grid -->
        <div
          class="absolute inset-0 bg-secondary/5 blur-3xl rounded-full transform rotate-12 scale-110 pointer-events-none"
        ></div>

        <div
          class="grid grid-cols-2 gap-4 relative z-10 w-full max-w-xs md:max-w-md transition-transform duration-700 ease-out"
        >
          <!-- Image 1 -->
          <div
            class="hero-grid-image aspect-square rounded-2xl overflow-hidden border border-white/10 shadow-lg group relative"
          >
            <img
              src="https://images.unsplash.com/photo-1560250097-0b93528c311a?ixlib=rb-1.2.1&auto=format&fit=crop&w=600&q=80"
              alt="Speaker 1"
              class="w-full h-full object-cover transition-transform duration-700 group-hover:scale-110 grayscale group-hover:grayscale-0"
            />
            <div
              class="absolute inset-0 bg-primary/20 group-hover:bg-transparent transition-colors"
            ></div>
          </div>
          <!-- Image 2 -->
          <div
            class="hero-grid-image aspect-square rounded-2xl overflow-hidden border border-white/10 shadow-lg group relative mt-8"
          >
            <img
              src="https://images.unsplash.com/photo-1519085360753-af0119f7cbe7?ixlib=rb-1.2.1&auto=format&fit=crop&w=600&q=80"
              alt="Speaker 2"
              class="w-full h-full object-cover transition-transform duration-700 group-hover:scale-110 grayscale group-hover:grayscale-0"
            />
            <div
              class="absolute inset-0 bg-primary/20 group-hover:bg-transparent transition-colors"
            ></div>
          </div>
          <!-- Image 3 -->
          <div
            class="hero-grid-image aspect-square rounded-2xl overflow-hidden border border-white/10 shadow-lg group relative -mt-8"
          >
            <img
              src="https://images.unsplash.com/photo-1475721027767-p05fa6e20db7?ixlib=rb-1.2.1&auto=format&fit=crop&w=600&q=80"
              alt="Speaker 3"
              class="w-full h-full object-cover transition-transform duration-700 group-hover:scale-110 grayscale group-hover:grayscale-0"
            />
            <div
              class="absolute inset-0 bg-primary/20 group-hover:bg-transparent transition-colors"
            ></div>
          </div>
          <!-- Image 4 -->
          <div
            class="hero-grid-image aspect-square rounded-2xl overflow-hidden border border-white/10 shadow-lg group relative"
          >
            <img
              src="https://images.unsplash.com/photo-1557804506-669a67965ba0?ixlib=rb-1.2.1&auto=format&fit=crop&w=600&q=80"
              alt="Speaker 4"
              class="w-full h-full object-cover transition-transform duration-700 group-hover:scale-110 grayscale group-hover:grayscale-0"
            />
            <div
              class="absolute inset-0 bg-primary/20 group-hover:bg-transparent transition-colors"
            ></div>
          </div>
        </div>
      </div>
    </div>

    <!-- Soundwave Bottom -->
    <div
      class="absolute bottom-10 left-0 w-full flex justify-center opacity-50 z-10 pointer-events-none"
    >
      <div class="soundwave-container h-16 flex items-center gap-1">
        <div class="bar" style="animation-delay: 0s"></div>
        <div class="bar" style="animation-delay: 0.2s"></div>
        <div class="bar" style="animation-delay: 0.4s"></div>
        <div class="bar" style="animation-delay: 0.1s"></div>
        <div class="bar" style="animation-delay: 0.5s"></div>
        <div class="bar" style="animation-delay: 0.3s"></div>
        <div class="bar" style="animation-delay: 0s"></div>
        <div class="bar" style="animation-delay: 0.2s"></div>
        <div class="bar" style="animation-delay: 0.4s"></div>
      </div>
    </div>
  </section>
</template>

<style scoped>
.soundwave-container .bar {
  width: 6px;
  height: 10px;
  background: #00e0ff;
  border-radius: 4px;
  animation: sound 1.5s ease-in-out infinite;
  box-shadow: 0 0 10px rgba(0, 224, 255, 0.5);
}
@keyframes sound {
  0%,
  100% {
    height: 10px;
    opacity: 0.3;
  }
  50% {
    height: 60px;
    opacity: 1;
  }
}

.mask-gradient {
  mask-image: linear-gradient(
    to right,
    transparent,
    black 10%,
    black 90%,
    transparent
  );
  -webkit-mask-image: linear-gradient(
    to right,
    transparent,
    black 10%,
    black 90%,
    transparent
  );
}

.animate-marquee-reverse {
  animation: marquee 30s linear infinite reverse;
}

@keyframes marquee {
  0% {
    transform: translateX(0);
  }
  100% {
    transform: translateX(-50%);
  }
}
</style>
