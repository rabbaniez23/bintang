<script setup>
defineProps({
  number: {
    type: String, // Or Number, but String allows "500+"
    required: true,
  },
  label: {
    type: String,
    required: true,
  },
  percentage: {
    type: Number,
    default: 0,
  },
});
</script>

<template>
  <div class="text-center p-6">
    <!-- Counter Value -->
    <div class="text-5xl font-bold text-white mb-2 drop-shadow-sm font-display">
      {{ number }}
    </div>

    <!-- Label -->
    <div class="text-lg font-medium text-white/90 mb-4">{{ label }}</div>

    <!-- Progress Bar (Requested in update) -->
    <div class="w-full h-2 bg-white/20 rounded-full overflow-hidden relative">
      <div
        class="h-full bg-cyan-accent rounded-full transition-all duration-1000 ease-out"
        :style="{ width: `${percentage}%` }"
      ></div>
    </div>
    <div class="text-right text-xs text-white/70 mt-1">
      {{ percentage }}% Proficiency
    </div>
  </div>
</template>
