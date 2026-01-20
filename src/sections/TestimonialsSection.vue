<script setup></script>

<template>
  <section
    class="py-24 relative overflow-hidden bg-primary border-t border-white/5"
  >
    <div
      class="absolute inset-0 bg-[url('https://www.transparenttextures.com/patterns/carbon-fibre.png')] opacity-5"
    ></div>

    <div class="max-w-7xl mx-auto px-6 lg:px-8 relative z-10">
      <div class="text-center mb-16">
        <span
          class="text-secondary font-display font-medium uppercase tracking-widest text-xs"
          >Testimoni</span
        >
        <h2 class="text-4xl font-display font-bold text-white mt-2">
          APA KATA MEREKA
        </h2>
      </div>

      <!-- Testimonial Scroller (Marquee) -->
      <div class="relative w-full overflow-hidden mask-gradient py-4">
        <div class="flex gap-8 whitespace-nowrap animate-marquee">
          <!-- Item 1 -->
          <div
            class="w-[400px] md:w-[500px] shrink-0 bg-surface/50 p-10 border border-white/5 relative hover:border-secondary/30 transition-all hover:-translate-y-1 hover:shadow-neon rounded-xl"
          >
            <span
              class="material-symbols-outlined text-6xl text-white/5 absolute top-6 right-6"
              >format_quote</span
            >
            <p
              class="text-slate-300 text-lg leading-relaxed italic mb-8 relative z-10 font-light whitespace-normal"
            >
              "Benar-benar menggetarkan. Cara dia membedah paradigma teknologi
              yang kompleks menjadi sesuatu yang mudah dipahami sungguh jenius."
            </p>
            <div class="flex items-center gap-4">
              <div
                class="w-12 h-12 rounded-full border border-secondary bg-gray-700 overflow-hidden"
              >
                <img
                  src="https://randomuser.me/api/portraits/men/32.jpg"
                  alt="User"
                  class="w-full h-full object-cover"
                />
              </div>
              <div>
                <h4
                  class="text-white font-bold font-display uppercase tracking-wide text-sm"
                >
                  Marcus Chen
                </h4>
                <p class="text-secondary text-xs uppercase tracking-widest">
                  CEO, TechGlobal
                </p>
              </div>
            </div>
          </div>

          <!-- Item 2 -->
          <div
            class="w-[400px] md:w-[500px] shrink-0 bg-surface/50 p-10 border border-white/5 relative hover:border-secondary/30 transition-all hover:-translate-y-1 hover:shadow-neon rounded-xl"
          >
            <span
              class="material-symbols-outlined text-6xl text-white/5 absolute top-6 right-6"
              >format_quote</span
            >
            <p
              class="text-slate-300 text-lg leading-relaxed italic mb-8 relative z-10 font-light whitespace-normal"
            >
              "Kami tidak hanya menginginkan pembicara; kami menginginkan
              seorang futuris yang bisa menantang dewan kami. Hasilnya melampaui
              ekspektasi."
            </p>
            <div class="flex items-center gap-4">
              <div
                class="w-12 h-12 rounded-full border border-secondary bg-gray-700 overflow-hidden"
              >
                <img
                  src="https://randomuser.me/api/portraits/women/44.jpg"
                  alt="User"
                  class="w-full h-full object-cover"
                />
              </div>
              <div>
                <h4
                  class="text-white font-bold font-display uppercase tracking-wide text-sm"
                >
                  Sarah Jenkins
                </h4>
                <p class="text-secondary text-xs uppercase tracking-widest">
                  Director, Future Fund
                </p>
              </div>
            </div>
          </div>

          <!-- Item 3 -->
          <div
            class="w-[400px] md:w-[500px] shrink-0 bg-surface/50 p-10 border border-white/5 relative hover:border-secondary/30 transition-all hover:-translate-y-1 hover:shadow-neon rounded-xl"
          >
            <span
              class="material-symbols-outlined text-6xl text-white/5 absolute top-6 right-6"
              >format_quote</span
            >
            <p
              class="text-slate-300 text-lg leading-relaxed italic mb-8 relative z-10 font-light whitespace-normal"
            >
              "Seorang visioner sejati yang memberikan cetak biru untuk strategi
              transformasi digital kami. Sangat direkomendasikan."
            </p>
            <div class="flex items-center gap-4">
              <div
                class="w-12 h-12 rounded-full border border-secondary bg-gray-700 overflow-hidden"
              >
                <img
                  src="https://randomuser.me/api/portraits/men/85.jpg"
                  alt="User"
                  class="w-full h-full object-cover"
                />
              </div>
              <div>
                <h4
                  class="text-white font-bold font-display uppercase tracking-wide text-sm"
                >
                  David Miller
                </h4>
                <p class="text-secondary text-xs uppercase tracking-widest">
                  CTO, InnovateX
                </p>
              </div>
            </div>
          </div>

          <!-- Duplicate for seamless loop -->
          <div
            class="w-[400px] md:w-[500px] shrink-0 bg-surface/50 p-10 border border-white/5 relative hover:border-secondary/30 transition-all hover:-translate-y-1 hover:shadow-neon rounded-xl"
          >
            <span
              class="material-symbols-outlined text-6xl text-white/5 absolute top-6 right-6"
              >format_quote</span
            >
            <p
              class="text-slate-300 text-lg leading-relaxed italic mb-8 relative z-10 font-light whitespace-normal"
            >
              "Benar-benar menggetarkan. Cara dia membedah paradigma teknologi
              yang kompleks menjadi sesuatu yang mudah dipahami sungguh jenius."
            </p>
            <div class="flex items-center gap-4">
              <div
                class="w-12 h-12 rounded-full border border-secondary bg-gray-700 overflow-hidden"
              >
                <img
                  src="https://randomuser.me/api/portraits/men/32.jpg"
                  alt="User"
                  class="w-full h-full object-cover"
                />
              </div>
              <div>
                <h4
                  class="text-white font-bold font-display uppercase tracking-wide text-sm"
                >
                  Marcus Chen
                </h4>
                <p class="text-secondary text-xs uppercase tracking-widest">
                  CEO, TechGlobal
                </p>
              </div>
            </div>
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
  animation: marquee 20s linear infinite;
}

.animate-marquee-reverse {
  animation: marquee 25s linear infinite reverse;
}

@keyframes marquee {
  0% {
    transform: translateX(0);
  }
  100% {
    transform: translateX(-50%);
  } /* Sesuikan dengan container width */
}
</style>
