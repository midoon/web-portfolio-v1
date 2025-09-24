<template>
  <section
    class="flex flex-col justify-center items-center text-primary-text min-h-screen"
  >
    <div class="flex flex-col justify-center items-start">
      <p data-aos="fade-right" class="text-xl font-roboto md:ml-2">
        Hello, I'm
      </p>
      <p
        data-aos="fade-right"
        class="text-7xl md:text-9xl font-roboto font-bold gap-0 md:tracking-widest"
      >
        HARUN
      </p>
      <div class="h-6 overflow-hidden self-end">
        <span id="role" class="inline-block align-top text-xl lg:mr-2"></span>
      </div>
    </div>
  </section>
</template>

<script setup>
import { onMounted, onBeforeUnmount } from "vue";
import Typed from "typed.js";

let typedInstance;

onMounted(() => {
  typedInstance = new Typed("#role", {
    strings: ["Back-End Developer", "Full-Stack Developer"],
    typeSpeed: 50,
    backSpeed: 50,
    loop: true,
  });
});

onBeforeUnmount(() => {
  // destroy instance supaya nggak memory leak
  typedInstance.destroy();
});
</script>
