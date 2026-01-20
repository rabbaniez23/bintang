<script setup>
import { onMounted } from "vue";
import TheNavbar from "./components/organisms/TheNavbar.vue";
import TheFooter from "./components/organisms/TheFooter.vue";
// import HomeView is handled by router or direct import if simple SPA
import HomeView from "./views/HomeView.vue";
</script>

<template>
  <div class="relative min-h-screen bg-primary">
    <!-- Global Grid Background (Fixed) -->
    <div
      class="fixed inset-0 z-0 pointer-events-none opacity-40 bg-grid-pattern"
    ></div>

    <!-- Navbar -->
    <TheNavbar />

    <!-- Main Content -->
    <div class="relative z-10">
      <HomeView />
    </div>

    <!-- Footer -->
    <TheFooter class="relative z-10" />
  </div>
</template>

<style>
/* Ensure grid pattern works */
.bg-grid-pattern {
  background-image:
    linear-gradient(to right, #1d3557 1px, transparent 1px),
    linear-gradient(to bottom, #1d3557 1px, transparent 1px);
  background-size: 50px 50px;
}
</style>
