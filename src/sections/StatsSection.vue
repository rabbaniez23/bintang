<script setup>
import { onMounted, ref } from "vue";
import { gsap } from "gsap";
import { ScrollTrigger } from "gsap/ScrollTrigger";

gsap.registerPlugin(ScrollTrigger);

const statsRef = ref(null);

const stats = [
  { value: 15, suffix: "+", label: "Tahun Pengalaman", icon: "history" },
  { value: 50, suffix: "+", label: "Keynote Global", icon: "public" },
  { value: 500, suffix: "k+", label: "Orang Terdampak", icon: "groups" },
  { value: 4.9, suffix: "", label: "Rating Rata-rata", icon: "star" },
];

onMounted(() => {
  // Use set first to ensure they are hidden if JS runs, but fallback to visible if not
  const elements = gsap.utils.toArray(".stat-card");

  // Animate from invisible to visible
  gsap.fromTo(
    elements,
    { y: 50, opacity: 0 },
    {
      scrollTrigger: {
        trigger: statsRef.value,
        start: "top 90%", // Trigger earlier
        toggleActions: "play none none reverse",
      },
      y: 0,
      opacity: 1,
      duration: 0.8,
      stagger: 0.15,
      ease: "back.out(1.7)",
    },
  );
});
</script>

<template>
  <section
    ref="statsRef"
    class="relative py-20 bg-surface border-y border-white/5 overflow-hidden"
  >
    <!-- Background Elements -->
    <div
      class="absolute top-0 right-0 w-full h-full bg-linear-to-b from-primary/50 to-transparent pointer-events-none"
    ></div>

    <div class="max-w-7xl mx-auto px-6 lg:px-8 relative z-10">
      <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-6">
        <div
          v-for="(item, index) in stats"
          :key="index"
          class="stat-card group relative p-8 rounded-2xl border border-white/10 bg-white/5 backdrop-blur-md hover:bg-white/10 hover:border-secondary/50 transition-all duration-300 hover:shadow-neon"
        >
          <div class="flex flex-col items-center text-center">
            <div
              class="w-14 h-14 mb-6 rounded-full bg-primary border border-secondary/30 flex items-center justify-center text-secondary group-hover:scale-110 transition-transform duration-500 shadow-lg shadow-black/20"
            >
              <span class="material-symbols-outlined text-3xl">{{
                item.icon
              }}</span>
            </div>

            <h3
              class="text-5xl font-display font-bold text-white mb-2 group-hover:text-secondary transition-colors duration-300"
            >
              {{ item.value
              }}<span
                class="text-3xl text-slate-500 group-hover:text-secondary/70"
                >{{ item.suffix }}</span
              >
            </h3>

            <p
              class="text-sm font-medium uppercase tracking-widest text-slate-400 group-hover:text-white transition-colors duration-300"
            >
              {{ item.label }}
            </p>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>
