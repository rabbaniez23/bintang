<script setup></script>

<template>
  <footer
    class="bg-black border-t border-white/10 pt-20 pb-10 px-6 lg:px-8"
    id="contact"
  >
    <div
      class="max-w-7xl mx-auto grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-12 mb-16"
    >
      <!-- Brand -->
      <div class="col-span-1 md:col-span-2">
        <div class="flex items-center gap-3 mb-6">
          <span class="material-symbols-outlined text-secondary text-3xl"
            >mic_external_on</span
          >
          <span
            class="text-2xl font-display font-bold text-white tracking-tighter"
            >BINTANG<span class="text-secondary">RAMADAN</span></span
          >
        </div>
        <p class="text-slate-400 text-sm leading-relaxed max-w-md mb-8">
          Membangun narasi positif melalui dakwah kreatif dan inovasi digital.
          Mari berkolaborasi untuk menciptakan dampak yang lebih luas bagi umat
          dan bangsa.
        </p>
        <div class="flex gap-4">
          <a
            href="#"
            class="w-10 h-10 border border-white/20 flex items-center justify-center text-white hover:bg-secondary hover:text-primary hover:border-secondary transition-all rounded-full"
          >
            <span class="font-bold text-sm">Ig</span>
          </a>
          <a
            href="#"
            class="w-10 h-10 border border-white/20 flex items-center justify-center text-white hover:bg-secondary hover:text-primary hover:border-secondary transition-all rounded-full"
          >
            <span class="font-bold text-sm">Yt</span>
          </a>
          <a
            href="#"
            class="w-10 h-10 border border-white/20 flex items-center justify-center text-white hover:bg-secondary hover:text-primary hover:border-secondary transition-all rounded-full"
          >
            <span class="font-bold text-sm">Lk</span>
          </a>
        </div>
      </div>

      <!-- Nav -->
      <div>
        <h4
          class="font-display font-bold text-white mb-6 uppercase tracking-wider text-sm"
        >
          Eksplorasi
        </h4>
        <ul class="space-y-3 text-sm text-slate-500">
          <li>
            <a href="#about" class="hover:text-secondary transition-colors"
              >Tentang Saya</a
            >
          </li>
          <li>
            <a href="#expertise" class="hover:text-secondary transition-colors"
              >Jejak Pendidikan</a
            >
          </li>
          <li>
            <a href="#gallery" class="hover:text-secondary transition-colors"
              >Dokumentasi</a
            >
          </li>
          <li>
            <a href="#portfolio" class="hover:text-secondary transition-colors"
              >Karya & Kontribusi</a
            >
          </li>
        </ul>
      </div>

      <!-- Contact Info -->
      <div>
        <h4
          class="font-display font-bold text-white mb-6 uppercase tracking-wider text-sm"
        >
          Hubungi Saya
        </h4>
        <ul class="space-y-4 text-sm text-slate-500">
          <li class="flex items-center gap-3">
            <span class="material-symbols-outlined text-secondary text-sm"
              >mail</span
            >
            salam@bintang.com
          </li>
          <li class="flex items-center gap-3">
            <span class="material-symbols-outlined text-secondary text-sm"
              >call</span
            >
            +62 812-9876-5432
          </li>
          <li class="flex items-center gap-3">
            <span class="material-symbols-outlined text-secondary text-sm"
              >location_on</span
            >
            Bandung, Indonesia
          </li>
        </ul>
      </div>
    </div>

    <!-- Bottom Bar -->
    <div
      class="max-w-7xl mx-auto pt-8 border-t border-white/5 flex flex-col md:flex-row justify-between items-center gap-4 text-slate-600 text-[10px] uppercase tracking-widest"
    >
      <div>© 2026 Bintang Ramadan. All Rights Reserved.</div>
      <div class="flex gap-8">
        <a href="#" class="hover:text-white transition-colors"
          >Privacy Policy</a
        >
        <a href="#" class="hover:text-white transition-colors"
          >Terms of Service</a
        >
      </div>
    </div>
  </footer>
</template>
