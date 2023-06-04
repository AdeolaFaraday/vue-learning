<script setup>
import TipContainer from "./components/TipContainer.vue";
</script>

<template>
  <div class="container">
    <TipContainer />
  </div>
</template>

<style scoped>
@import url("https://fonts.googleapis.com/css2?family=Dosis:wght@300;400;500&family=Roboto+Mono:wght@400;500&family=Space+Mono:wght@400;700&display=swap");
@tailwind base;
@tailwind components;
@tailwind utilities;

@layer components {
  .container {
    font-family: "Roboto Mono", sans-serif;
    @apply flex justify-center lg:items-center items-end max-w-full h-screen;
    background-color: #e6fffd;
  }
}
</style>
