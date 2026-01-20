<script setup>
import { ref, onMounted, onUnmounted } from "vue";

const isScrolled = ref(false);
const isMobileMenuOpen = ref(false);

const handleScroll = () => {
  // Ubah state saat scroll lebih dari 50px
  isScrolled.value = window.scrollY > 50;
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
    class="fixed left-0 right-0 z-50 transition-all duration-500 ease-in-out"
    :class="
      isScrolled
        ? 'top-4 px-4 md:px-0' // Saat scroll: Melayang & ada jarak atas
        : 'top-0 px-0' // Saat diatas: Full width
    "
  >
    <div
      class="mx-auto transition-all duration-500 flex items-center justify-between"
      :class="
        isScrolled
          ? 'max-w-5xl glass-panel rounded-2xl h-16 shadow-neon/20 border-white/10 px-6' // Style kapsul saat scroll
          : 'max-w-7xl h-24 bg-transparent px-6 lg:px-8 border-transparent' // Style transparan saat diatas
      "
    >
      <div class="flex items-center gap-2 group cursor-pointer">
        <div class="relative w-8 h-8 flex items-center justify-center overflow-hidden rounded-lg">
           <div class="absolute inset-0 bg-secondary/20 group-hover:bg-secondary/40 transition-all"></div>
           <span class="material-symbols-outlined text-secondary text-sm font-bold">mic_external_on</span>
        </div>
        
        <div class="flex flex-col">
          <span class="text-lg font-display font-bold text-white tracking-tight leading-none group-hover:text-secondary transition-colors">
            NAUFAL<span class="font-light opacity-80">RIZKI</span>
          </span>
          <span v-if="!isScrolled" class="text-[9px] text-slate-400 tracking-[0.3em] uppercase mt-1 opacity-0 md:opacity-100 transition-opacity duration-300">
            Educator & Speaker
          </span>
        </div>
      </div>

      <div class="hidden md:flex items-center gap-8">
        <a v-for="item in ['Beranda', 'Tentang', 'Topik']" 
           :key="item"
           :href="`#${item.toLowerCase()}`"
           class="text-[12px] font-medium text-slate-300 hover:text-secondary hover:glow-text transition-all tracking-[0.15em] uppercase relative group"
        >
          {{ item }}
          <span class="absolute -bottom-1 left-0 w-0 h-[1px] bg-secondary transition-all duration-300 group-hover:w-full"></span>
        </a>

        <a
          href="#contact"
          class="px-5 py-2 rounded-lg bg-secondary/10 border border-secondary/30 text-secondary font-display font-bold text-[10px] uppercase tracking-widest hover:bg-secondary hover:text-primary hover:shadow-neon transition-all duration-300 transform hover:-translate-y-0.5"
        >
          Undang Bicara
        </a>
      </div>

      <button class="md:hidden text-white hover:text-secondary transition-colors" @click="toggleMobileMenu">
        <span class="material-symbols-outlined">menu_open</span>
      </button>
    </div>

    <transition
      enter-active-class="transition duration-200 ease-out"
      enter-from-class="transform -translate-y-4 opacity-0"
      enter-to-class="transform translate-y-0 opacity-100"
      leave-active-class="transition duration-150 ease-in"
      leave-from-class="transform translate-y-0 opacity-100"
      leave-to-class="transform -translate-y-4 opacity-0"
    >
      <div
        v-if="isMobileMenuOpen"
        class="absolute top-full left-4 right-4 mt-2 glass-panel rounded-xl p-6 flex flex-col gap-4 shadow-xl border border-white/10"
      >
        <a href="#home" class="text-slate-300 hover:text-secondary text-sm font-medium">Beranda</a>
        <a href="#about" class="text-slate-300 hover:text-secondary text-sm font-medium">Tentang</a>
        <a href="#expertise" class="text-slate-300 hover:text-secondary text-sm font-medium">Topik</a>
        <a href="#contact" class="text-secondary font-bold text-sm">Undang Bicara</a>
      </div>
    </transition>
  </nav>
</template>