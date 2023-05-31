<script setup>
import TipContainer from "./components/TipContainer.vue";
</script>

<template>
  <div class="container">
    <TipContainer />
  </div>
</template>

<style scoped>
@tailwind base;
@tailwind components;
@tailwind utilities;

@layer components {
  /* h1 {
    @apply font-bold underline;
  } */
  .container {
    @apply flex justify-center items-center w-full h-screen;
    background-color: #e6fffd;
  }
}
</style>
