<script setup>
defineProps({
  title: {
    type: String,
    required: true,
  },
  description: {
    type: String,
    required: true,
  },
  icon: {
    type: String, // Can be a URL or an SVG string if using inline SVG components
    default: "",
  },
});
</script>

<template>
  <div
    class="bg-white rounded-xl shadow-md hover:shadow-xl transition-all duration-300 p-8 border border-gray-100 group hover:-translate-y-2 cursor-default"
  >
    <div
      class="w-16 h-16 bg-gradient-to-br from-primary-blue to-ocean-blue rounded-lg flex items-center justify-center mb-6 group-hover:scale-110 transition-transform duration-300 shadow-blue-glow"
    >
      <slot name="icon">
        <!-- Default Icon Placeholder if slot is empty -->
        <svg
          class="w-8 h-8 text-white"
          fill="none"
          stroke="currentColor"
          viewBox="0 0 24 24"
        >
          <path
            stroke-linecap="round"
            stroke-linejoin="round"
            stroke-width="2"
            d="M13 10V3L4 14h7v7l9-11h-7z"
          />
        </svg>
      </slot>
    </div>
    <h3
      class="text-2xl font-bold text-charcoal mb-3 group-hover:text-primary-blue transition-colors duration-200"
    >
      {{ title }}
    </h3>
    <p class="text-base text-dark-gray leading-relaxed mb-4">
      {{ description }}
    </p>
    <div
      class="inline-flex items-center text-primary-blue font-semibold hover:text-ocean-blue transition-colors duration-200 cursor-pointer"
    >
      Learn More
      <svg
        class="w-4 h-4 ml-2 group-hover:translate-x-1 transition-transform duration-200"
        fill="none"
        stroke="currentColor"
        viewBox="0 0 24 24"
      >
        <path
          stroke-linecap="round"
          stroke-linejoin="round"
          stroke-width="2"
          d="M9 5l7 7-7 7"
        />
      </svg>
    </div>
  </div>
</template>
