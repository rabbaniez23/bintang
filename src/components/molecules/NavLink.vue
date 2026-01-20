<script setup>
defineProps({
  href: {
    type: String,
    required: true,
  },
  active: {
    type: Boolean,
    default: false,
  },
});
</script>

<template>
  <a
    :href="href"
    class="relative font-medium text-dark-gray hover:text-primary-blue transition-colors duration-200 py-2 group"
    :class="{ 'text-primary-blue': active }"
  >
    <slot></slot>
    <span
      class="absolute bottom-0 left-0 w-0 h-0.5 bg-primary-blue transition-all duration-300 group-hover:w-full"
      :class="{ 'w-full': active }"
    ></span>
  </a>
</template>
