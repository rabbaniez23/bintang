<script setup>
import { onMounted, ref } from "vue";
import { gsap } from "gsap";
import { ScrollTrigger } from "gsap/ScrollTrigger";

gsap.registerPlugin(ScrollTrigger);

const galleryRef = ref(null);

const galleryImages = [
  "https://images.unsplash.com/photo-1544531696-60c35eb8d626?ixlib=rb-1.2.1&auto=format&fit=crop&w=800&q=80",
  "https://images.unsplash.com/photo-1515168816178-541c851c597d?ixlib=rb-1.2.1&auto=format&fit=crop&w=800&q=80",
  "https://images.unsplash.com/photo-1475721027767-p05fa6e20db7?ixlib=rb-1.2.1&auto=format&fit=crop&w=800&q=80",
  "https://images.unsplash.com/photo-1560250097-0b93528c311a?ixlib=rb-1.2.1&auto=format&fit=crop&w=800&q=80",
  "https://images.unsplash.com/photo-1557804506-669a67965ba0?ixlib=rb-1.2.1&auto=format&fit=crop&w=800&q=80",
  "https://images.unsplash.com/photo-1519085360753-af0119f7cbe7?ixlib=rb-1.2.1&auto=format&fit=crop&w=800&q=80",
];

onMounted(() => {
  gsap.from(".gallery-item", {
    scrollTrigger: {
      trigger: galleryRef.value,
      start: "top 70%",
    },
    y: 50,
    opacity: 0,
    duration: 0.8,
    stagger: 0.1,
    ease: "power2.out",
  });
});
</script>

<template>
  <section
    ref="galleryRef"
    class="py-24 bg-primary relative overflow-hidden"
    id="gallery"
  >
    <!-- Header -->
    <div class="max-w-7xl mx-auto px-6 lg:px-8 mb-12 text-center">
      <span
        class="text-secondary font-display font-medium tracking-[0.2em] uppercase text-sm mb-2 block"
        >// Dokumentasi</span
      >
      <h2 class="text-3xl md:text-5xl font-display font-bold text-white mb-6">
        MOMEN DI ATAS PANGGUNG
      </h2>
      <p class="text-slate-400 max-w-2xl mx-auto text-lg font-light">
        Rekaman jejak perjalanan dalam menyebarkan ide dan inspirasi di berbagai
        panggung nasional dan internasional.
      </p>
    </div>

    <!-- Masonry-ish Grid -->
    <div class="max-w-7xl mx-auto px-6 lg:px-8">
      <div class="columns-1 md:columns-2 lg:columns-3 gap-6 space-y-6">
        <div
          v-for="(img, index) in galleryImages"
          :key="index"
          class="gallery-item break-inside-avoid relative group rounded-xl overflow-hidden shadow-lg border border-white/5"
        >
          <img
            :src="img"
            alt="Event Gallery"
            class="w-full h-auto object-cover transform group-hover:scale-110 transition-transform duration-700 whitespace-pre-wrap"
          />
          <div
            class="absolute inset-0 bg-gradient-to-t from-primary/90 to-transparent opacity-0 group-hover:opacity-100 transition-opacity duration-300 flex items-end p-6"
          >
            <span
              class="text-white font-display font-bold uppercase tracking-widest text-sm"
              >Tech Conference {{ 2023 + (index % 2) }}</span
            >
          </div>
        </div>
      </div>
    </div>
  </section>
</template>
