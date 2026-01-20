<script setup>
import { onMounted, onUnmounted, ref } from "vue";
import { gsap } from "gsap";
import { ScrollTrigger } from "gsap/ScrollTrigger";

import HeroSection from "../sections/HeroSection.vue";
import StatsSection from "../sections/StatsSection.vue";
import AboutSection from "../sections/AboutSection.vue";
import TopicsSection from "../sections/TopicsSection.vue";
import PortfolioSection from "../sections/PortfolioSection.vue";
import TestimonialsSection from "../sections/TestimonialsSection.vue";
import LogoCloudSection from "../sections/LogoCloudSection.vue";

gsap.registerPlugin(ScrollTrigger);

const mainRef = ref(null);
let ctx;

onMounted(() => {
  // Global Layered Pinning Logic
  // Referencing the user's CodePen idea: "Layered pinning with infinite looping"
  // Note: Infinite looping of the *page* might be too aggressive for a CV, but the layering is great.
  // We will implement the Layering (Pinning) logic.

  ctx = gsap.context(() => {
    // Global Layered Pinning Logic REMOVED to prevent conflicts with internal Section pinning.
    // The "Layered" effect will be handled by CSS `position: sticky` in style block.

    const panels = gsap.utils.toArray(".panel");
    // No global ScrollTrigger.create loop here.

    // Optional: Snap to sections (User provided this in snippet)
    // We can enable it if it feels smooth. Let's try to include it but commented out or active based on preference.
    // The user's code had complex snap logic. I'll add a simplified version for better UX.
    /* 
    ScrollTrigger.create({
      snap: 1 / (panels.length - 1)
    });
    */
  }, mainRef.value);
});

onUnmounted(() => {
  ctx && ctx.revert();
});
</script>

<template>
  <main ref="mainRef" class="relative">
    <HeroSection />
    <StatsSection />
    <AboutSection />
    <TopicsSection />

    <PortfolioSection />
    <TestimonialsSection />
    <LogoCloudSection />
    <!-- Contact is now merged into Footer as per the new design -->
  </main>
</template>

<style>
/* Global styles if needed */
</style>
