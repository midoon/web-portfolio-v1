<template>
  <header class="flex justify-between items-center p-8 lg:px-12 relative z-20">
    <div class="text-primary-text text-3xl font-bold">LOGO</div>

    <!-- mobile toggle button -->
    <div class="md:hidden z-30">
      <button
        class="block focus:outline-none"
        @click="isMenuOpen = !isMenuOpen"
      >
        <span v-if="isMenuOpen" class="text-5xl text-primary-text">
          <Icon icon="material-symbols:close-rounded" />
        </span>
        <span v-else class="text-5xl text-primary-text">
          <Icon icon="material-symbols:menu" />
        </span>
      </button>
    </div>

    <!-- navbar link -->
    <nav
      :class="[
        `fixed inset-0 z-20 flex flex-col items-center justify-center bg-primary-background md:relative md:bg-transparent md:flex md:justify-between md:flex-row ${
          isMenuOpen ? 'blobk' : 'hidden'
        }`,
      ]"
    >
      <ul
        class="flex flex-col items-center space-y-5 md:flex-row md:space-x-5 md:space-y-0"
      >
        <li v-for="item in Menu" :key="item.name">
          <a
            :href="item.href"
            class="block transition ease-linear md:text-xl font-bold text-secondary-text hover:text-primary-text"
            @click="scrollToSection(item.href)"
            >{{ item.name }}</a
          >
        </li>
      </ul>
    </nav>
  </header>
</template>

<script setup>
import { ref } from "vue";

const isMenuOpen = ref(false);

const Menu = ref([
  { name: "About Me", href: "#aboutme" },
  { name: "Skills", href: "#skills" },
  { name: "Projects", href: "#projects" },
  { name: "Contact", href: "#contact" },
]);

const scrollToSection = (href) => {
  isMenuOpen.value = false;
  const section = document.querySelector(href);
  if (section) {
    section.scrollIntoView({ behavior: "smooth" });
  }
};
</script>
