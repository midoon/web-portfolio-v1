<template>
  <section id="skills" class="bg-accent-background py-20">
    <p
      data-aos="fade-up"
      class="text-primary-text text-center text-3xl font-roboto underline-offset-8 underline mb-10"
    >
      Skills
    </p>
    <div
      class="grid grid-cols-2 lg:max-w-[80vw] lg:grid-cols-4 lg:mx-auto gap-6 px-8"
    >
      <!-- card skill -->
      <div v-for="skill in skills" :key="skill.name" class="">
        <div
          data-aos="flip-up"
          class="bg-primary-background rounded-lg p-6 flex flex-col items-center text-center h-full hover:scale-105 transition-transform duration-300 lg:flex-row"
        >
          <img :src="skill.icon" :alt="skill.name" class="w-16 h-16 mb-4" />
          <div class="lg:text-left lg:ml-6">
            <h3 class="text-xl font-semibold mb-2 text-primary-text">
              {{ skill.name }}
            </h3>
            <p class="hidden text-secondary-text lg:block lg:text-sm">
              {{ skill.description }}
            </p>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>
<script setup>
const skills = [
  {
    name: "Javascript",
    description: "Programming Language",
    icon: new URL(`@/assets/skill-icon/JavaScript.svg`, import.meta.url).href,
  },
  {
    name: "Node.Js",
    description: "Javascript runtime",
    icon: new URL(`@/assets/skill-icon/Node.js.svg`, import.meta.url).href,
  },
  {
    name: "Golang",
    description: "Programming language",
    icon: new URL(`@/assets/skill-icon/Go.svg`, import.meta.url).href,
  },
  {
    name: "PHP",
    description: "Programming language",
    icon: new URL(`@/assets/skill-icon/PHP.svg`, import.meta.url).href,
  },
  {
    name: "Python",
    description: "Programming language",
    icon: new URL(`@/assets/skill-icon/Python.svg`, import.meta.url).href,
  },
  {
    name: "Express.JS",
    description: "Javascript Framework",
    icon: new URL(`@/assets/skill-icon/Express.svg`, import.meta.url).href,
  },
  {
    name: "Fiber",
    description: "Golang Framework",
    icon: new URL(`@/assets/skill-icon/fiber.png`, import.meta.url).href,
  },
  {
    name: "Laravel",
    description: "PHP Framework",
    icon: new URL(`@/assets/skill-icon/Laravel.svg`, import.meta.url).href,
  },
  {
    name: "Flask",
    description: "Python Framework",
    icon: new URL(`@/assets/skill-icon/Flask.svg`, import.meta.url).href,
  },
  {
    name: "Vue.JS",
    description: "Javascript Framework",
    icon: new URL(`@/assets/skill-icon/Vue.js.svg`, import.meta.url).href,
  },
  {
    name: "HTML",
    description: "Markup Framework",
    icon: new URL(`@/assets/skill-icon/HTML5.svg`, import.meta.url).href,
  },
  {
    name: "CSS",
    description: "Style sheets",
    icon: new URL(`@/assets/skill-icon/CSS3.svg`, import.meta.url).href,
  },
  {
    name: "Tailwind CSS",
    description: "Utility framework",
    icon: new URL(`@/assets/skill-icon/Tailwind-CSS.svg`, import.meta.url).href,
  },
  {
    name: "REST API",
    description: "Web service",
    icon: new URL(`@/assets/skill-icon/api.png`, import.meta.url).href,
  },
  {
    name: "Google Cloud Platform",
    description: "Cloud services",
    icon: new URL(`@/assets/skill-icon/Google-Cloud.svg`, import.meta.url).href,
  },
  {
    name: "Amazon Web Service",
    description: "Cloud services",
    icon: new URL(`@/assets/skill-icon/AWS.svg`, import.meta.url).href,
  },
  {
    name: "Docker",
    description: "Container platform",
    icon: new URL(`@/assets/skill-icon/Docker.svg`, import.meta.url).href,
  },
  {
    name: "Git",
    description: "Version control",
    icon: new URL(`@/assets/skill-icon/Git.svg`, import.meta.url).href,
  },
];
</script>
<style></style>
