<script setup>
import { defineAsyncComponent } from "vue";
const Navbar = defineAsyncComponent(() =>
  import("@/components/layout/Navbar.vue")
);

const HeroSection = defineAsyncComponent(() =>
  import("@/components/layout/HeroSection.vue")
);

const AboutSection = defineAsyncComponent(() =>
  import("@/components/layout/AboutSection.vue")
);
</script>

<template>
  <div class="min-h-screen bg-primary-background">
    <Navbar />
    <HeroSection />
    <AboutSection />
  </div>
</template>
