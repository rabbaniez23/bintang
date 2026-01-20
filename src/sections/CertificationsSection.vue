<script setup>
import { onMounted, ref } from "vue";
import { gsap } from "gsap";
import { ScrollTrigger } from "gsap/ScrollTrigger";

gsap.registerPlugin(ScrollTrigger);

const certRef = ref(null);

const certifications = [
  {
    name: "Certified Public Speaker",
    issuer: "IPS Empire",
    year: "2023",
    icon: "record_voice_over",
    description:
      "Profesional speaker certification dengan fokus pada audiens korporat.",
  },
  {
    name: "Digital Transformation Spec.",
    issuer: "Google Cloud",
    year: "2024",
    icon: "cloud_done",
    description:
      "Sertifikasi keahlian dalam strategi transformasi digital enterprise.",
  },
  {
    name: "Master of Ceremony",
    issuer: "Talk Inc.",
    year: "2022",
    icon: "mic",
    description:
      "Sertifikasi pembawa acara formal dan non-formal tingkat nasional.",
  },
  {
    name: "Communication Strategist",
    issuer: "LinkedIn Learning",
    year: "2023",
    icon: "campaign",
    description: "Strategi komunikasi efektif untuk pimpinan dan eksekutif.",
  },
];

onMounted(() => {
  gsap.from(".cert-card", {
    scrollTrigger: {
      trigger: certRef.value,
      start: "top 80%",
    },
    y: 50,
    opacity: 0,
    duration: 0.8,
    stagger: 0.2,
    ease: "power2.out",
  });
});
</script>

<template>
  <section
    ref="certRef"
    class="py-24 bg-surface border-t border-white/5 relative overflow-hidden"
    id="certifications"
  >
    <div class="max-w-7xl mx-auto px-6 lg:px-8 relative z-10">
      <div
        class="flex flex-col md:flex-row justify-between items-end mb-16 gap-6"
      >
        <div>
          <span
            class="text-secondary font-display font-medium tracking-[0.2em] uppercase text-sm mb-2 block"
            >// Kredibilitas</span
          >
          <h2 class="text-3xl md:text-4xl font-display font-bold text-white">
            SERTIFIKASI PROFESIONAL
          </h2>
        </div>
        <p class="text-slate-400 max-w-md text-sm leading-relaxed">
          Dedikasi terhadap keunggulan melalui pembelajaran berkelanjutan dan
          validasi profesional.
        </p>
      </div>

      <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-6">
        <div
          v-for="(cert, index) in certifications"
          :key="index"
          class="cert-card group relative bg-primary/50 border border-white/10 p-6 rounded-lg hover:border-secondary/50 transition-all duration-300"
        >
          <div
            class="absolute top-4 right-4 opacity-10 group-hover:opacity-100 transition-opacity"
          >
            <span class="material-symbols-outlined text-4xl text-secondary">{{
              cert.icon
            }}</span>
          </div>

          <div class="mb-6 mt-2">
            <span
              class="inline-block px-3 py-1 rounded-full bg-secondary/10 text-secondary text-xs font-bold mb-3"
              >{{ cert.year }}</span
            >
            <h3
              class="text-xl font-display font-bold text-white mb-1 group-hover:text-secondary transition-colors"
            >
              {{ cert.name }}
            </h3>
            <p class="text-slate-500 text-sm italic">{{ cert.issuer }}</p>
          </div>

          <p
            class="text-slate-400 text-sm leading-relaxed border-t border-white/5 pt-4"
          >
            {{ cert.description }}
          </p>
        </div>
      </div>
    </div>
  </section>
</template>
