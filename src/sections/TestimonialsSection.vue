<script setup>
import { onMounted, ref } from "vue";
import { gsap } from "gsap";
import { ScrollTrigger } from "gsap/ScrollTrigger";

gsap.registerPlugin(ScrollTrigger);

const testimonialRef = ref(null);

onMounted(() => {
  const ctx = gsap.context(() => {
    // Animasi Header
    gsap.from(".testi-header-anim", {
      scrollTrigger: {
        trigger: testimonialRef.value,
        start: "top 80%",
        toggleActions: "play reverse play reverse",
      },
      y: 30,
      opacity: 0,
      duration: 1,
      ease: "power2.out",
    });

    // Animasi Container Marquee (Muncul pelan)
    gsap.from(".testi-marquee-anim", {
      scrollTrigger: {
        trigger: testimonialRef.value,
        start: "top 75%",
        toggleActions: "play reverse play reverse",
      },
      opacity: 0,
      duration: 1.5,
      delay: 0.3,
      ease: "power2.out",
    });
  }, testimonialRef.value);
});
</script>

<template>
  <section
    ref="testimonialRef"
    class="py-32 bg-primary relative overflow-hidden"
    id="testimonials"
  >
    <div
      class="absolute inset-0 bg-grid-pattern opacity-20 pointer-events-none"
    ></div>
    <div
      class="absolute top-[-10%] left-[20%] w-[500px] h-[500px] bg-secondary/10 rounded-full blur-[120px] animate-pulse-slow pointer-events-none"
    ></div>
    <div
      class="absolute bottom-[-10%] right-[20%] w-[400px] h-[400px] bg-accent/10 rounded-full blur-[100px] animate-pulse-slow pointer-events-none"
    ></div>
    <div class="max-w-7xl mx-auto px-6 lg:px-8 relative z-10">
      <div class="text-center mb-16 testi-header-anim">
        <span
          class="text-secondary font-display font-bold tracking-[0.2em] uppercase text-sm mb-4 block"
        >
          // Stories of Impact
        </span>
        <h2
          class="text-4xl md:text-6xl font-display font-bold text-white tracking-tight"
        >
          KATA
          <span
            class="text-transparent bg-clip-text bg-gradient-to-r from-secondary to-accent"
            >MEREKA</span
          >
        </h2>
        <p
          class="text-slate-400 max-w-2xl mx-auto text-lg font-light leading-relaxed mt-4"
        >
          Testimoni jujur dari jamaah, panitia acara, dan teman-teman komunitas
          yang pernah berkolaborasi.
        </p>
      </div>

      <div
        class="relative w-full overflow-hidden mask-gradient py-8 testi-marquee-anim"
      >
        <div class="flex gap-8 whitespace-nowrap animate-marquee">
          <div
            class="w-[400px] md:w-[450px] shrink-0 bg-surface-light p-8 border border-white/5 rounded-2xl relative hover:border-secondary/30 transition-all hover:-translate-y-1 hover:shadow-neon/20 group whitespace-normal"
          >
            <span
              class="material-symbols-outlined text-6xl text-white/5 absolute top-6 right-6 group-hover:text-secondary/10 transition-colors"
              >format_quote</span
            >
            <p
              class="text-slate-300 text-lg leading-relaxed italic mb-8 relative z-10 font-light"
            >
              "Penyampaian Kak Bintang itu 'daging' banget tapi santai.
              Anak-anak muda di kampus jadi betah dengerin kajian berjam-jam
              tanpa ngerasa digurui."
            </p>
            <div class="flex items-center gap-4">
              <div
                class="w-12 h-12 rounded-full border border-secondary/50 overflow-hidden"
              >
                <img
                  src="https://images.unsplash.com/photo-1599566150163-29194dcaad36?ixlib=rb-1.2.1&auto=format&fit=crop&w=200&q=80"
                  alt="User"
                  class="w-full h-full object-cover"
                />
              </div>
              <div>
                <h4
                  class="text-white font-bold font-display uppercase tracking-wide text-sm"
                >
                  Rizky Pratama
                </h4>
                <p class="text-secondary text-xs uppercase tracking-widest">
                  Ketua DKM Kampus
                </p>
              </div>
            </div>
          </div>

          <div
            class="w-[400px] md:w-[450px] shrink-0 bg-surface-light p-8 border border-white/5 rounded-2xl relative hover:border-secondary/30 transition-all hover:-translate-y-1 hover:shadow-neon/20 group whitespace-normal"
          >
            <span
              class="material-symbols-outlined text-6xl text-white/5 absolute top-6 right-6 group-hover:text-secondary/10 transition-colors"
              >format_quote</span
            >
            <p
              class="text-slate-300 text-lg leading-relaxed italic mb-8 relative z-10 font-light"
            >
              "Jujur baru kali ini nemu konten dakwah yang visualnya estetik dan
              bahasanya relate sama struggle kita sebagai Gen-Z. Keep
              inspiring!"
            </p>
            <div class="flex items-center gap-4">
              <div
                class="w-12 h-12 rounded-full border border-secondary/50 overflow-hidden"
              >
                <img
                  src="https://images.unsplash.com/photo-1494790108377-be9c29b29330?ixlib=rb-1.2.1&auto=format&fit=crop&w=200&q=80"
                  alt="User"
                  class="w-full h-full object-cover"
                />
              </div>
              <div>
                <h4
                  class="text-white font-bold font-display uppercase tracking-wide text-sm"
                >
                  Sarah Amalia
                </h4>
                <p class="text-secondary text-xs uppercase tracking-widest">
                  Follower Instagram
                </p>
              </div>
            </div>
          </div>

          <div
            class="w-[400px] md:w-[450px] shrink-0 bg-surface-light p-8 border border-white/5 rounded-2xl relative hover:border-secondary/30 transition-all hover:-translate-y-1 hover:shadow-neon/20 group whitespace-normal"
          >
            <span
              class="material-symbols-outlined text-6xl text-white/5 absolute top-6 right-6 group-hover:text-secondary/10 transition-colors"
              >format_quote</span
            >
            <p
              class="text-slate-300 text-lg leading-relaxed italic mb-8 relative z-10 font-light"
            >
              "Kami mengundang beliau untuk sesi sharing session leadership.
              Alhamdulillah feedback peserta sangat positif, energinya nular
              banget!"
            </p>
            <div class="flex items-center gap-4">
              <div
                class="w-12 h-12 rounded-full border border-secondary/50 overflow-hidden"
              >
                <img
                  src="https://images.unsplash.com/photo-1507003211169-0a1dd7228f2d?ixlib=rb-1.2.1&auto=format&fit=crop&w=200&q=80"
                  alt="User"
                  class="w-full h-full object-cover"
                />
              </div>
              <div>
                <h4
                  class="text-white font-bold font-display uppercase tracking-wide text-sm"
                >
                  Fajar Nugraha
                </h4>
                <p class="text-secondary text-xs uppercase tracking-widest">
                  Founder Pemuda Hijrah
                </p>
              </div>
            </div>
          </div>

          <div
            class="w-[400px] md:w-[450px] shrink-0 bg-surface-light p-8 border border-white/5 rounded-2xl relative hover:border-secondary/30 transition-all hover:-translate-y-1 hover:shadow-neon/20 group whitespace-normal"
          >
            <span
              class="material-symbols-outlined text-6xl text-white/5 absolute top-6 right-6 group-hover:text-secondary/10 transition-colors"
              >format_quote</span
            >
            <p
              class="text-slate-300 text-lg leading-relaxed italic mb-8 relative z-10 font-light"
            >
              "Penyampaian Kak Bintang itu 'daging' banget tapi santai.
              Anak-anak muda di kampus jadi betah dengerin kajian berjam-jam
              tanpa ngerasa digurui."
            </p>
            <div class="flex items-center gap-4">
              <div
                class="w-12 h-12 rounded-full border border-secondary/50 overflow-hidden"
              >
                <img
                  src="https://images.unsplash.com/photo-1599566150163-29194dcaad36?ixlib=rb-1.2.1&auto=format&fit=crop&w=200&q=80"
                  alt="User"
                  class="w-full h-full object-cover"
                />
              </div>
              <div>
                <h4
                  class="text-white font-bold font-display uppercase tracking-wide text-sm"
                >
                  Rizky Pratama
                </h4>
                <p class="text-secondary text-xs uppercase tracking-widest">
                  Ketua DKM Kampus
                </p>
              </div>
            </div>
          </div>
          <div
            class="w-[400px] md:w-[450px] shrink-0 bg-surface-light p-8 border border-white/5 rounded-2xl relative hover:border-secondary/30 transition-all hover:-translate-y-1 hover:shadow-neon/20 group whitespace-normal"
          >
            <span
              class="material-symbols-outlined text-6xl text-white/5 absolute top-6 right-6 group-hover:text-secondary/10 transition-colors"
              >format_quote</span
            >
            <p
              class="text-slate-300 text-lg leading-relaxed italic mb-8 relative z-10 font-light"
            >
              "Jujur baru kali ini nemu konten dakwah yang visualnya estetik dan
              bahasanya relate sama struggle kita sebagai Gen-Z. Keep
              inspiring!"
            </p>
            <div class="flex items-center gap-4">
              <div
                class="w-12 h-12 rounded-full border border-secondary/50 overflow-hidden"
              >
                <img
                  src="https://images.unsplash.com/photo-1494790108377-be9c29b29330?ixlib=rb-1.2.1&auto=format&fit=crop&w=200&q=80"
                  alt="User"
                  class="w-full h-full object-cover"
                />
              </div>
              <div>
                <h4
                  class="text-white font-bold font-display uppercase tracking-wide text-sm"
                >
                  Sarah Amalia
                </h4>
                <p class="text-secondary text-xs uppercase tracking-widest">
                  Follower Instagram
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
/* Gradient Mask untuk efek fade di kiri-kanan marquee */
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
  animation: marquee 30s linear infinite;
}

@keyframes marquee {
  0% {
    transform: translateX(0);
  }
  100% {
    transform: translateX(-50%);
  } /* Karena kita menduplikasi item, geser 50% cukup */
}

/* Animasi Pulse untuk Orbs */
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
