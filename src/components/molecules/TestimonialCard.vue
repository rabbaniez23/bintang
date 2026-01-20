<script setup>
defineProps({
  name: {
    type: String,
    required: true,
  },
  role: {
    type: String,
    default: "",
  },
  quote: {
    type: String,
    required: true,
  },
  avatar: {
    type: String,
    default: "",
  },
});
</script>

<template>
  <div
    class="bg-light-gray rounded-lg p-6 border-l-4 border-cyan-accent shadow-sm hover:shadow-md transition-shadow duration-200"
  >
    <div class="flex items-start gap-4">
      <img
        :src="avatar || 'https://ui-avatars.com/api/?name=' + name"
        :alt="name"
        class="w-16 h-16 rounded-full shadow-md object-cover"
      />
      <div class="flex-1">
        <p class="text-base text-dark-gray italic leading-relaxed mb-4">
          "{{ quote }}"
        </p>
        <div>
          <p class="font-semibold text-charcoal">{{ name }}</p>
          <p v-if="role" class="text-sm text-medium-gray">{{ role }}</p>
        </div>
      </div>
    </div>
  </div>
</template>
