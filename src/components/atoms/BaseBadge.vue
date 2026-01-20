<script setup>
import { computed } from "vue";

const props = defineProps({
  variant: {
    type: String,
    default: "skill", // 'skill', 'status-success', 'status-warning'
    validator: (value) =>
      ["skill", "status-success", "status-warning"].includes(value),
  },
  text: {
    type: String,
    required: true,
  },
});

const badgeClasses = computed(() => {
  switch (props.variant) {
    case "skill":
      return "bg-cyan-accent/10 text-primary-blue border-cyan-accent/30";
    case "status-success":
      return "bg-success-green/10 text-success-green border-success-green/20";
    case "status-warning":
      return "bg-warning-amber/10 text-warning-amber border-warning-amber/20";
    default:
      return "bg-gray-100 text-gray-800";
  }
});
</script>

<template>
  <span
    class="inline-block px-4 py-2 rounded-full text-sm font-medium border"
    :class="badgeClasses"
  >
    {{ text }}
  </span>
</template>
