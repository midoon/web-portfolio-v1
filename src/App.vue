<script setup>
import { defineAsyncComponent } from "vue";
const Navbar = defineAsyncComponent(() =>
  import("@/components/layout/Navbar.vue")
);

const HeroSection = defineAsyncComponent(() =>
  import("@/components/layout/HeroSection.vue")
);
</script>

<template>
  <div class="min-h-screen bg-primary-background">
    <Navbar />
    <HeroSection />
  </div>
</template>
