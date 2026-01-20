<script setup>
import { ref, onMounted, onUnmounted } from "vue";

const isScrolled = ref(false);
const isMobileMenuOpen = ref(false);

const handleScroll = () => {
  isScrolled.value = window.scrollY > 20;
};

const toggleMobileMenu = () => {
  isMobileMenuOpen.value = !isMobileMenuOpen.value;
};

onMounted(() => {
  window.addEventListener("scroll", handleScroll);
});

onUnmounted(() => {
  window.removeEventListener("scroll", handleScroll);
});
</script>

<template>
  <nav
    class="fixed top-0 w-full z-50 transition-all duration-300 border-b border-white/5"
    :class="isScrolled ? 'glass-panel h-20' : 'bg-transparent h-24'"
  >
    <div class="max-w-7xl mx-auto px-6 lg:px-8 h-full">
      <div class="flex justify-between items-center h-full">
        <!-- Logo -->
        <div class="flex items-center gap-3 group cursor-pointer">
          <div class="relative w-10 h-10 flex items-center justify-center">
            <div
              class="absolute inset-0 border border-secondary/30 rounded-full group-hover:animate-ping opacity-20"
            ></div>
            <div
              class="absolute inset-0 border border-secondary rounded-full group-hover:shadow-neon transition-all duration-300"
            ></div>
            <span class="material-symbols-outlined text-secondary text-lg"
              >graphic_eq</span
            >
          </div>
          <div>
            <span
              class="text-xl font-display font-bold text-white tracking-tighter"
              >TECH<span class="text-secondary">SPEAKER</span></span
            >
            <p
              class="text-[9px] text-secondary tracking-[0.2em] uppercase leading-none"
            >
              Innovate. Lead.
            </p>
          </div>
        </div>

        <!-- Desktop Menu -->
        <div class="hidden md:flex items-center gap-10">
          <a
            class="text-sm font-medium text-slate-300 hover:text-secondary hover:glow-text transition-all tracking-wide uppercase"
            href="#home"
            >Beranda</a
          >
          <a
            class="text-sm font-medium text-slate-300 hover:text-secondary hover:glow-text transition-all tracking-wide uppercase"
            href="#about"
            >Tentang</a
          >
          <a
            class="text-sm font-medium text-slate-300 hover:text-secondary hover:glow-text transition-all tracking-wide uppercase"
            href="#expertise"
            >Topik</a
          >
          <a
            class="relative px-6 py-2 bg-transparent border border-secondary text-secondary font-display font-bold uppercase tracking-widest text-xs hover:bg-secondary hover:text-primary hover:shadow-neon transition-all duration-300 group overflow-hidden"
            href="#contact"
          >
            <span class="relative z-10">Kontak</span>
            <div
              class="absolute inset-0 bg-secondary transform -translate-x-full group-hover:translate-x-0 transition-transform duration-300 ease-out -z-0"
            ></div>
          </a>
        </div>

        <!-- Mobile Toggle -->
        <div
          class="md:hidden text-white cursor-pointer"
          @click="toggleMobileMenu"
        >
          <span class="material-symbols-outlined text-3xl">menu</span>
        </div>
      </div>
    </div>

    <!-- Mobile Menu Overlay -->
    <div
      v-if="isMobileMenuOpen"
      class="absolute top-full left-0 w-full bg-surface border-b border-white/10 p-6 flex flex-col gap-4 shadow-xl"
    >
      <a
        href="#home"
        class="text-slate-300 hover:text-secondary uppercase tracking-widest text-sm"
        >Beranda</a
      >
      <a
        href="#about"
        class="text-slate-300 hover:text-secondary uppercase tracking-widest text-sm"
        >Tentang</a
      >
      <a
        href="#expertise"
        class="text-slate-300 hover:text-secondary uppercase tracking-widest text-sm"
        >Topik</a
      >
      <a
        href="#contact"
        class="text-secondary font-bold uppercase tracking-widest text-sm"
        >Kontak</a
      >
    </div>
  </nav>
</template>
