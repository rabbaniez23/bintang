<script setup>
defineProps({
  modelValue: {
    type: [String, Number],
    default: "",
  },
  label: {
    type: String,
    default: "",
  },
  placeholder: {
    type: String,
    default: "",
  },
  type: {
    type: String,
    default: "text",
  },
  id: {
    type: String,
    required: true,
  },
});

defineEmits(["update:modelValue"]);
</script>

<template>
  <div class="flex flex-col gap-2 w-full">
    <label
      v-if="label"
      :for="id"
      class="text-sm font-semibold text-charcoal ml-1"
    >
      {{ label }}
    </label>
    <input
      :id="id"
      :type="type"
      :placeholder="placeholder"
      :value="modelValue"
      @input="$emit('update:modelValue', $event.target.value)"
      class="w-full px-4 py-3 border-2 border-gray-300 rounded-lg text-dark-gray placeholder-medium-gray focus:border-primary-blue focus:ring-2 focus:ring-primary-blue/20 focus:outline-none transition-all duration-200 bg-white"
    />
  </div>
</template>
