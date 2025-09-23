<script setup>
import { defineAsyncComponent } from "vue";
const Navbar = defineAsyncComponent(() =>
  import("@/components/layout/Navbar.vue")
);
</script>

<template>
  <div class="min-h-screen bg-primary-background">
    <Navbar />
  </div>
</template>
