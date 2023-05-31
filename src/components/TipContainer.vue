<script setup></script>
<template>
  <div class="container"></div>
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
    @apply h-3/5 w-3/5 rounded-2xl;
    background-color: #fff;
  }
}
</style>
