<script setup></script>

<template>
  <section
    class="py-24 bg-surface border-y border-white/5 overflow-hidden"
    id="portfolio"
  >
    <!-- Header -->
    <div
      class="max-w-7xl mx-auto px-6 lg:px-8 mb-12 flex items-end justify-between"
    >
      <div>
        <span
          class="text-secondary font-display font-medium tracking-[0.2em] uppercase text-sm mb-2 block"
          >Keterlibatan Global</span
        >
        <h2 class="text-4xl font-display font-bold text-white">
          PANGGUNG TERPILIH
        </h2>
      </div>
      <!-- Navigation Buttons (Optional/Removed for Grid) -->
      <div class="flex gap-4 hidden md:flex opacity-50 cursor-not-allowed">
        <!-- Kept for consistency but disabled for grid view -->
      </div>
    </div>

    <!-- Grid Container (3 cols x 2 rows = 6 items) -->
    <div
      class="max-w-7xl mx-auto px-6 lg:px-8 grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-6"
    >
      <!-- Card 1 -->
      <div
        class="group relative h-[320px] rounded-lg overflow-hidden border border-white/5 bg-primary cursor-pointer"
      >
        <img
          src="https://images.unsplash.com/photo-1544161515-4ab6ce6db874?ixlib=rb-1.2.1&auto=format&fit=crop&w=800&q=80"
          alt="Tech Summit"
          class="w-full h-full object-cover transition-transform duration-700 group-hover:scale-110 grayscale group-hover:grayscale-0 opacity-60 group-hover:opacity-100"
        />
        <div
          class="absolute inset-0 bg-linear-to-t from-primary via-primary/50 to-transparent opacity-90"
        ></div>

        <div
          class="absolute bottom-0 left-0 w-full p-6 transform translate-y-4 group-hover:translate-y-0 transition-transform duration-500"
        >
          <div class="flex items-center gap-2 mb-2">
            <span
              class="px-2 py-1 bg-secondary/20 text-secondary text-[10px] font-bold uppercase tracking-widest border border-secondary/20"
              >Keynote</span
            >
            <span class="text-slate-300 text-[10px] uppercase tracking-widest"
              >Berlin, 2023</span
            >
          </div>
          <h3 class="text-xl font-display font-bold text-white mb-1">
            Global Tech Summit
          </h3>
          <p
            class="text-slate-400 text-xs mb-4 line-clamp-2 opacity-0 group-hover:opacity-100 transition-opacity duration-500 delay-100"
          >
            Membahas "Etika Kesadaran Buatan" di hadapan 5.000 pengembang dan
            pembuat kebijakan.
          </p>
        </div>
      </div>

      <!-- Card 2 -->
      <div
        class="group relative h-[320px] rounded-lg overflow-hidden border border-white/5 bg-primary cursor-pointer"
      >
        <img
          src="https://images.unsplash.com/photo-1543269865-cbf427effbad?ixlib=rb-1.2.1&auto=format&fit=crop&w=800&q=80"
          alt="Leadership Retreat"
          class="w-full h-full object-cover transition-transform duration-700 group-hover:scale-110 grayscale group-hover:grayscale-0 opacity-60 group-hover:opacity-100"
        />
        <div
          class="absolute inset-0 bg-linear-to-t from-primary via-primary/50 to-transparent opacity-90"
        ></div>

        <div
          class="absolute bottom-0 left-0 w-full p-6 transform translate-y-4 group-hover:translate-y-0 transition-transform duration-500"
        >
          <div class="flex items-center gap-2 mb-2">
            <span
              class="px-2 py-1 bg-secondary/20 text-secondary text-[10px] font-bold uppercase tracking-widest border border-secondary/20"
              >Moderator</span
            >
            <span class="text-slate-300 text-[10px] uppercase tracking-widest"
              >Silicon Valley</span
            >
          </div>
          <h3 class="text-xl font-display font-bold text-white mb-1">
            Executive Retreat
          </h3>
          <p
            class="text-slate-400 text-xs mb-4 line-clamp-2 opacity-0 group-hover:opacity-100 transition-opacity duration-500 delay-100"
          >
            Memfasilitasi sesi strategi tingkat tinggi untuk eksekutif C-Suite
            perusahaan Fortune 100.
          </p>
        </div>
      </div>

      <!-- Card 3 -->
      <div
        class="group relative h-[320px] rounded-lg overflow-hidden border border-white/5 bg-primary cursor-pointer"
      >
        <img
          src="https://images.unsplash.com/photo-1559056216-2c5e52da3f78?ixlib=rb-1.2.1&auto=format&fit=crop&w=800&q=80"
          alt="Future Cities"
          class="w-full h-full object-cover transition-transform duration-700 group-hover:scale-110 grayscale group-hover:grayscale-0 opacity-60 group-hover:opacity-100"
        />
        <div
          class="absolute inset-0 bg-linear-to-t from-primary via-primary/50 to-transparent opacity-90"
        ></div>

        <div
          class="absolute bottom-0 left-0 w-full p-6 transform translate-y-4 group-hover:translate-y-0 transition-transform duration-500"
        >
          <div class="flex items-center gap-2 mb-2">
            <span
              class="px-2 py-1 bg-secondary/20 text-secondary text-[10px] font-bold uppercase tracking-widest border border-secondary/20"
              >Host</span
            >
            <span class="text-slate-300 text-[10px] uppercase tracking-widest"
              >Tokyo, 2024</span
            >
          </div>
          <h3 class="text-xl font-display font-bold text-white mb-1">
            Future Cities Expo
          </h3>
          <p
            class="text-slate-400 text-xs mb-4 line-clamp-2 opacity-0 group-hover:opacity-100 transition-opacity duration-500 delay-100"
          >
            Memandu acara imersif 3 hari yang memamerkan teknologi perkotaan
            abad berikutnya.
          </p>
        </div>
      </div>

      <!-- Card 4 (New) -->
      <div
        class="group relative h-[320px] rounded-lg overflow-hidden border border-white/5 bg-primary cursor-pointer"
      >
        <img
          src="https://images.unsplash.com/photo-1515187029135-18ee286d815b?ixlib=rb-1.2.1&auto=format&fit=crop&w=800&q=80"
          alt="AI Symposium"
          class="w-full h-full object-cover transition-transform duration-700 group-hover:scale-110 grayscale group-hover:grayscale-0 opacity-60 group-hover:opacity-100"
        />
        <div
          class="absolute inset-0 bg-linear-to-t from-primary via-primary/50 to-transparent opacity-90"
        ></div>

        <div
          class="absolute bottom-0 left-0 w-full p-6 transform translate-y-4 group-hover:translate-y-0 transition-transform duration-500"
        >
          <div class="flex items-center gap-2 mb-2">
            <span
              class="px-2 py-1 bg-secondary/20 text-secondary text-[10px] font-bold uppercase tracking-widest border border-secondary/20"
              >Panelis</span
            >
            <span class="text-slate-300 text-[10px] uppercase tracking-widest"
              >London, 2024</span
            >
          </div>
          <h3 class="text-xl font-display font-bold text-white mb-1">
            AI Ethics Symposium
          </h3>
          <p
            class="text-slate-400 text-xs mb-4 line-clamp-2 opacity-0 group-hover:opacity-100 transition-opacity duration-500 delay-100"
          >
            Mendebarkan implikasi moral AGI dengan filsuf terkemuka dunia.
          </p>
        </div>
      </div>

      <!-- Card 5 (New) -->
      <div
        class="group relative h-[320px] rounded-lg overflow-hidden border border-white/5 bg-primary cursor-pointer"
      >
        <img
          src="https://images.unsplash.com/photo-1521737604893-d14cc237f11d?ixlib=rb-1.2.1&auto=format&fit=crop&w=800&q=80"
          alt="TedX"
          class="w-full h-full object-cover transition-transform duration-700 group-hover:scale-110 grayscale group-hover:grayscale-0 opacity-60 group-hover:opacity-100"
        />
        <div
          class="absolute inset-0 bg-linear-to-t from-primary via-primary/50 to-transparent opacity-90"
        ></div>

        <div
          class="absolute bottom-0 left-0 w-full p-6 transform translate-y-4 group-hover:translate-y-0 transition-transform duration-500"
        >
          <div class="flex items-center gap-2 mb-2">
            <span
              class="px-2 py-1 bg-secondary/20 text-secondary text-[10px] font-bold uppercase tracking-widest border border-secondary/20"
              >Speaker</span
            >
            <span class="text-slate-300 text-[10px] uppercase tracking-widest"
              >Singapore, 2025</span
            >
          </div>
          <h3 class="text-xl font-display font-bold text-white mb-1">
            TEDx Marina Bay
          </h3>
          <p
            class="text-slate-400 text-xs mb-4 line-clamp-2 opacity-0 group-hover:opacity-100 transition-opacity duration-500 delay-100"
          >
            Menyampaikan pembicaraan viral "Kemanusiaan di Era Silikon".
          </p>
        </div>
      </div>

      <!-- Card 6 (New) -->
      <div
        class="group relative h-[320px] rounded-lg overflow-hidden border border-white/5 bg-primary cursor-pointer"
      >
        <img
          src="https://images.unsplash.com/photo-1475721027767-p05fa6e20db7?ixlib=rb-1.2.1&auto=format&fit=crop&w=800&q=80"
          alt="Cybersec Conf"
          class="w-full h-full object-cover transition-transform duration-700 group-hover:scale-110 grayscale group-hover:grayscale-0 opacity-60 group-hover:opacity-100"
        />
        <div
          class="absolute inset-0 bg-linear-to-t from-primary via-primary/50 to-transparent opacity-90"
        ></div>

        <div
          class="absolute bottom-0 left-0 w-full p-6 transform translate-y-4 group-hover:translate-y-0 transition-transform duration-500"
        >
          <div class="flex items-center gap-2 mb-2">
            <span
              class="px-2 py-1 bg-secondary/20 text-secondary text-[10px] font-bold uppercase tracking-widest border border-secondary/20"
              >Keynote</span
            >
            <span class="text-slate-300 text-[10px] uppercase tracking-widest"
              >New York, 2025</span
            >
          </div>
          <h3 class="text-xl font-display font-bold text-white mb-1">
            CyberSec World
          </h3>
          <p
            class="text-slate-400 text-xs mb-4 line-clamp-2 opacity-0 group-hover:opacity-100 transition-opacity duration-500 delay-100"
          >
            Opening keynote on the vulnerabilities of quantum cryptography.
          </p>
        </div>
      </div>
    </div>
  </section>
</template>
