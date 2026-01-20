<script setup></script>

<template>
  <section class="py-32 bg-primary relative" id="expertise">
    <div class="max-w-7xl mx-auto px-6 lg:px-8">
      <!-- Header -->
      <div
        class="flex flex-col md:flex-row justify-between items-end mb-20 gap-8"
      >
        <div>
          <span
            class="text-secondary font-display font-medium tracking-[0.2em] uppercase text-sm mb-2 block"
            >// Apa Yang Saya Tawarkan</span
          >
          <h2 class="text-4xl md:text-5xl font-display font-bold text-white">
            LAYANAN PROFESIONAL
          </h2>
        </div>
        <div class="h-px flex-grow bg-white/10 hidden md:block mx-8 mb-4"></div>
        <p class="text-slate-400 max-w-sm text-sm">
          Solusi profesional untuk kebutuhan acara, edukasi, dan strategi
          digital perusahaan Anda.
        </p>
      </div>

      <!-- Grid -->
      <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
        <!-- Card 1 -->
        <div
          class="group relative bg-surface hover:bg-surface-light p-10 transition-all duration-300 border border-white/5 hover:border-secondary/50 overflow-hidden"
        >
          <div
            class="absolute top-0 right-0 p-6 opacity-10 group-hover:opacity-20 transition-opacity"
          >
            <span class="material-symbols-outlined text-8xl text-secondary"
              >mic</span
            >
          </div>
          <div
            class="w-16 h-16 rounded-full border border-secondary/30 flex items-center justify-center mb-8 group-hover:shadow-neon transition-all bg-primary/50 backdrop-blur-sm"
          >
            <span class="material-symbols-outlined text-3xl text-secondary"
              >record_voice_over</span
            >
          </div>
          <h3
            class="text-2xl font-display font-bold text-white mb-4 group-hover:text-secondary transition-colors"
          >
            Seminar Speaker
          </h3>
          <p class="text-slate-400 text-sm leading-relaxed mb-8">
            Pembicara seminar dengan materi seputar Teknologi, Pengembangan
            Diri, dan Masa Depan Karir di Era Digital.
          </p>
          <a
            class="inline-flex items-center gap-2 text-secondary text-xs font-bold uppercase tracking-widest group-hover:gap-4 transition-all"
            href="#contact"
          >
            Undang Sekarang
            <span class="material-symbols-outlined text-sm">arrow_forward</span>
          </a>
        </div>

        <!-- Card 2 -->
        <div
          class="group relative bg-surface hover:bg-surface-light p-10 transition-all duration-300 border border-white/5 hover:border-secondary/50 overflow-hidden"
        >
          <div
            class="absolute top-0 right-0 p-6 opacity-10 group-hover:opacity-20 transition-opacity"
          >
            <span class="material-symbols-outlined text-8xl text-secondary"
              >campaign</span
            >
          </div>
          <div
            class="w-16 h-16 rounded-full border border-secondary/30 flex items-center justify-center mb-8 group-hover:shadow-neon transition-all bg-primary/50 backdrop-blur-sm"
          >
            <span class="material-symbols-outlined text-3xl text-secondary"
              >podium</span
            >
          </div>
          <h3
            class="text-2xl font-display font-bold text-white mb-4 group-hover:text-secondary transition-colors"
          >
            Master of Ceremony
          </h3>
          <p class="text-slate-400 text-sm leading-relaxed mb-8">
            Memandu acara formal maupun semi-formal dengan pembawaan yang
            energik, profesional, dan adaptif.
          </p>
          <a
            class="inline-flex items-center gap-2 text-secondary text-xs font-bold uppercase tracking-widest group-hover:gap-4 transition-all"
            href="#contact"
          >
            Booking Jadwal
            <span class="material-symbols-outlined text-sm">arrow_forward</span>
          </a>
        </div>

        <!-- Card 3 -->
        <div
          class="group relative bg-surface hover:bg-surface-light p-10 transition-all duration-300 border border-white/5 hover:border-secondary/50 overflow-hidden"
        >
          <div
            class="absolute top-0 right-0 p-6 opacity-10 group-hover:opacity-20 transition-opacity"
          >
            <span class="material-symbols-outlined text-8xl text-secondary"
              >school</span
            >
          </div>
          <div
            class="w-16 h-16 rounded-full border border-secondary/30 flex items-center justify-center mb-8 group-hover:shadow-neon transition-all bg-primary/50 backdrop-blur-sm"
          >
            <span class="material-symbols-outlined text-3xl text-secondary"
              >cast_for_education</span
            >
          </div>
          <h3
            class="text-2xl font-display font-bold text-white mb-4 group-hover:text-secondary transition-colors"
          >
            content Creator
          </h3>
          <p class="text-slate-400 text-sm leading-relaxed mb-8">
            Kolaborasi pembuatan konten edukasi teknologi untuk brand awareness
            dan edukasi pasar yang efektif.
          </p>
          <a
            class="inline-flex items-center gap-2 text-secondary text-xs font-bold uppercase tracking-widest group-hover:gap-4 transition-all"
            href="#contact"
          >
            Kolaborasi
            <span class="material-symbols-outlined text-sm">arrow_forward</span>
          </a>
        </div>
      </div>
    </div>
  </section>
</template>
