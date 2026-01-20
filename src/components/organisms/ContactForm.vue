<script setup>
import { ref } from "vue";
import BaseInput from "../atoms/BaseInput.vue";
import BaseButton from "../atoms/BaseButton.vue";

const form = ref({
  name: "",
  email: "",
  message: "",
});

const isSubmitting = ref(false);

const handleSubmit = async () => {
  isSubmitting.value = true;
  // Simulate API call
  await new Promise((resolve) => setTimeout(resolve, 1500));
  console.log("Form Submitted", form.value);
  alert("Message Sent! (Simulated)");
  isSubmitting.value = false;
  form.value = { name: "", email: "", message: "" };
};
</script>

<template>
  <form
    @submit.prevent="handleSubmit"
    class="space-y-6 max-w-2xl mx-auto bg-white p-8 rounded-2xl shadow-xl border border-gray-100"
  >
    <BaseInput
      id="name"
      label="Full Name"
      v-model="form.name"
      placeholder="Enter your name"
      required
    />
    <BaseInput
      id="email"
      label="Email Address"
      type="email"
      v-model="form.email"
      placeholder="your@email.com"
      required
    />

    <div class="flex flex-col gap-2 w-full">
      <label for="message" class="text-sm font-semibold text-charcoal ml-1"
        >Message</label
      >
      <textarea
        id="message"
        v-model="form.message"
        rows="5"
        class="w-full px-4 py-3 border-2 border-gray-300 rounded-lg text-dark-gray placeholder-medium-gray focus:border-primary-blue focus:ring-2 focus:ring-primary-blue/20 focus:outline-none transition-all duration-200 bg-white resize-none"
        placeholder="Tell us about your event..."
        required
      ></textarea>
    </div>

    <BaseButton
      type="submit"
      variant="primary"
      class="w-full"
      :disabled="isSubmitting"
    >
      {{ isSubmitting ? "Sending..." : "Send Message" }}
    </BaseButton>
  </form>
</template>
