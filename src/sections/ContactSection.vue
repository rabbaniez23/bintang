<script setup>
import ContactForm from "../components/organisms/ContactForm.vue";
</script>

<template>
  <section
    id="contact"
    class="py-24 bg-gradient-to-br from-navy-dark to-deep-blue relative panel z-60"
  >
    <div class="absolute inset-0 bg-[url('/grid-pattern.svg')] opacity-5"></div>
    <div
      class="max-w-7xl mx-auto px-6 grid grid-cols-1 lg:grid-cols-2 gap-16 items-center"
    >
      <div class="text-white">
        <h2 class="text-5xl font-display font-bold mb-6">Let's Collaborate</h2>
        <p class="text-xl text-white/80 mb-8 leading-relaxed">
          Ready to elevate your next event? Reach out to discuss availability,
          topics, and how we can create a memorable experience for your
          audience.
        </p>

        <div class="space-y-6">
          <div class="flex items-center gap-4">
            <div
              class="w-12 h-12 rounded-full bg-white/10 flex items-center justify-center text-cyan-accent"
            >
              <svg
                class="w-6 h-6"
                fill="none"
                stroke="currentColor"
                viewBox="0 0 24 24"
              >
                <path
                  stroke-linecap="round"
                  stroke-linejoin="round"
                  stroke-width="2"
                  d="M3 8l7.89 5.26a2 2 0 002.22 0L21 8M5 19h14a2 2 0 002-2V7a2 2 0 00-2-2H5a2 2 0 00-2 2v10a2 2 0 002 2z"
                />
              </svg>
            </div>
            <div>
              <p class="text-sm text-white/60">Email</p>
              <p class="text-lg font-semibold">contact@bintangdocs.com</p>
            </div>
          </div>

          <div class="flex items-center gap-4">
            <div
              class="w-12 h-12 rounded-full bg-white/10 flex items-center justify-center text-cyan-accent"
            >
              <svg
                class="w-6 h-6"
                fill="none"
                stroke="currentColor"
                viewBox="0 0 24 24"
              >
                <path
                  stroke-linecap="round"
                  stroke-linejoin="round"
                  stroke-width="2"
                  d="M17.657 16.657L13.414 20.9a1.998 1.998 0 01-2.827 0l-4.244-4.243a8 8 0 1111.314 0z"
                />
                <path
                  stroke-linecap="round"
                  stroke-linejoin="round"
                  stroke-width="2"
                  d="M15 11a3 3 0 11-6 0 3 3 0 016 0z"
                />
              </svg>
            </div>
            <div>
              <p class="text-sm text-white/60">Location</p>
              <p class="text-lg font-semibold">Jakarta, Indonesia</p>
            </div>
          </div>
        </div>
      </div>

      <div>
        <ContactForm />
      </div>
    </div>
  </section>
</template>
