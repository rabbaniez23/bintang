<script setup></script>

<template>
  <section class="py-16 bg-primary border-t border-white/5 overflow-hidden">
    <div class="max-w-7xl mx-auto px-6 lg:px-8 text-center">
      <p class="text-slate-500 text-[10px] uppercase tracking-[0.3em] mb-10">
        Dipercaya Oleh Komunitas & Brand
      </p>

      <div class="relative overflow-hidden mask-gradient w-full max-w-5xl mx-auto">
        <div class="flex gap-16 items-center whitespace-nowrap animate-marquee opacity-60 hover:opacity-100 transition-opacity duration-500">
          
          <div class="text-2xl font-display font-bold text-white/40 hover:text-secondary transition-colors cursor-default">HIJRAHFEST</div>
          <div class="text-2xl font-display font-bold text-white/40 hover:text-secondary transition-colors cursor-default">KAHF EVERYDAY</div>
          <div class="text-2xl font-display font-bold text-white/40 hover:text-secondary transition-colors cursor-default">WARDAH</div>
          <div class="text-2xl font-display font-bold text-white/40 hover:text-secondary transition-colors cursor-default">BANK SYARIAH</div>
          <div class="text-2xl font-display font-bold text-white/40 hover:text-secondary transition-colors cursor-default">DOMPET DHUAFA</div>
          <div class="text-2xl font-display font-bold text-white/40 hover:text-secondary transition-colors cursor-default">YUKNGAJI</div>
          <div class="text-2xl font-display font-bold text-white/40 hover:text-secondary transition-colors cursor-default">RABBANI</div>
          <div class="text-2xl font-display font-bold text-white/40 hover:text-secondary transition-colors cursor-default">ISLAM ITU INDAH</div>

          <div class="text-2xl font-display font-bold text-white/40 hover:text-secondary transition-colors cursor-default">HIJRAHFEST</div>
          <div class="text-2xl font-display font-bold text-white/40 hover:text-secondary transition-colors cursor-default">KAHF EVERYDAY</div>
          <div class="text-2xl font-display font-bold text-white/40 hover:text-secondary transition-colors cursor-default">WARDAH</div>
          <div class="text-2xl font-display font-bold text-white/40 hover:text-secondary transition-colors cursor-default">BANK SYARIAH</div>
          <div class="text-2xl font-display font-bold text-white/40 hover:text-secondary transition-colors cursor-default">DOMPET DHUAFA</div>
          <div class="text-2xl font-display font-bold text-white/40 hover:text-secondary transition-colors cursor-default">YUKNGAJI</div>
          <div class="text-2xl font-display font-bold text-white/40 hover:text-secondary transition-colors cursor-default">RABBANI</div>
          <div class="text-2xl font-display font-bold text-white/40 hover:text-secondary transition-colors cursor-default">ISLAM ITU INDAH</div>

        </div>
      </div>
    </div>
  </section>
</template>

<style scoped>
/* Efek Fade di kiri kanan agar marquee terlihat keluar dari kegelapan */
.mask-gradient {
  mask-image: linear-gradient(to right, transparent, black 10%, black 90%, transparent);
  -webkit-mask-image: linear-gradient(to right, transparent, black 10%, black 90%, transparent);
}

.animate-marquee {
  animation: marquee 40s linear infinite;
}

@keyframes marquee {
  0% { transform: translateX(0); }
  100% { transform: translateX(-50%); }
}
</style>