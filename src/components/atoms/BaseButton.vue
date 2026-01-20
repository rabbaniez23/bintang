<script setup>
import { computed } from "vue";

const props = defineProps({
  variant: {
    type: String,
    default: "primary",
    validator: (value) => ["primary", "secondary", "ghost"].includes(value),
  },
  label: {
    type: String,
    default: "",
  },
  type: {
    type: String,
    default: "button",
  },
  disabled: {
    type: Boolean,
    default: false,
  },
});

const variantClasses = computed(() => {
  switch (props.variant) {
    case "primary":
      return "bg-gradient-to-r from-primary-blue to-deep-blue text-white shadow-lg shadow-primary-blue/30 hover:shadow-primary-blue/50 hover:-translate-y-1 border border-transparent";
    case "secondary":
      return "bg-transparent border-2 border-primary-blue text-primary-blue hover:bg-primary-blue hover:text-white hover:shadow-lg hover:shadow-primary-blue/30 hover:-translate-y-1";
    case "ghost":
      return "text-primary-blue bg-transparent hover:bg-light-gray/50 hover:text-deep-blue";
    default:
      return "bg-primary-blue text-white";
  }
});
</script>

<template>
  <button
    :type="type"
    :disabled="disabled"
    class="relative px-8 py-3 rounded-full font-bold tracking-wide transition-all duration-300 flex items-center justify-center gap-2 cursor-pointer disabled:opacity-50 disabled:cursor-not-allowed group overflow-hidden active:scale-95"
    :class="variantClasses"
  >
    <!-- Shine Effect for Primary -->
    <div
      v-if="variant === 'primary'"
      class="absolute inset-0 -translate-x-full group-hover:animate-[shimmer_1.5s_infinite] bg-gradient-to-r from-transparent via-white/20 to-transparent z-0 pointer-events-none"
    ></div>

    <span class="relative z-10 font-mono flex items-center gap-2">
      <slot name="prefix"></slot>
      <span v-if="label">{{ label }}</span>
      <slot>{{ !label ? "Button" : "" }}</slot>
      <slot name="suffix"></slot>
    </span>
  </button>
</template>
