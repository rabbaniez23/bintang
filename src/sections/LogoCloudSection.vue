<script setup></script>

<template>
  <section class="py-20 bg-primary border-t border-white/5 overflow-hidden">
    <div class="max-w-7xl mx-auto px-6 lg:px-8 text-center">
      <p class="text-slate-500 text-xs uppercase tracking-[0.3em] mb-12">
        Diliput Oleh Media Ternama
      </p>

      <div
        class="relative overflow-hidden mask-gradient w-full max-w-5xl mx-auto"
      >
        <div
          class="flex gap-16 items-center whitespace-nowrap animate-marquee opacity-50 hover:opacity-100 transition-opacity duration-500"
        >
          <!-- Logo Items (Text as placeholder for now, can be replaced with SVGs) -->
          <div
            class="text-3xl font-display font-bold text-white/50 hover:text-white transition-colors"
          >
            WIRED
          </div>
          <div
            class="text-3xl font-display font-bold text-white/50 hover:text-white transition-colors"
          >
            TechCrunch
          </div>
          <div
            class="text-3xl font-display font-bold text-white/50 hover:text-white transition-colors"
          >
            TheVerge
          </div>
          <div
            class="text-3xl font-display font-bold text-white/50 hover:text-white transition-colors"
          >
            FastCompany
          </div>
          <div
            class="text-3xl font-display font-bold text-white/50 hover:text-white transition-colors"
          >
            Forbes
          </div>
          <div
            class="text-3xl font-display font-bold text-white/50 hover:text-white transition-colors"
          >
            Bloomberg
          </div>
          <div
            class="text-3xl font-display font-bold text-white/50 hover:text-white transition-colors"
          >
            CNN Indonesia
          </div>
          <div
            class="text-3xl font-display font-bold text-white/50 hover:text-white transition-colors"
          >
            Kompas
          </div>

          <!-- Duplicates for seamless loop -->
          <div
            class="text-3xl font-display font-bold text-white/50 hover:text-white transition-colors"
          >
            WIRED
          </div>
          <div
            class="text-3xl font-display font-bold text-white/50 hover:text-white transition-colors"
          >
            TechCrunch
          </div>
          <div
            class="text-3xl font-display font-bold text-white/50 hover:text-white transition-colors"
          >
            TheVerge
          </div>
          <div
            class="text-3xl font-display font-bold text-white/50 hover:text-white transition-colors"
          >
            FastCompany
          </div>
          <div
            class="text-3xl font-display font-bold text-white/50 hover:text-white transition-colors"
          >
            Forbes
          </div>
          <div
            class="text-3xl font-display font-bold text-white/50 hover:text-white transition-colors"
          >
            Bloomberg
          </div>
          <div
            class="text-3xl font-display font-bold text-white/50 hover:text-white transition-colors"
          >
            CNN Indonesia
          </div>
          <div
            class="text-3xl font-display font-bold text-white/50 hover:text-white transition-colors"
          >
            Kompas
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped>
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

.animate-marquee {
  animation: marquee 40s linear infinite;
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
