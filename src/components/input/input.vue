<script setup></script>
<template>
  <div>
    <input type="text" class="input" />
  </div>
</template>

<style scoped>
@tailwind base;
@tailwind components;
@tailwind utilities;

@layer components {
  .input {
    @apply h-12 px-6 rounded w-full focus:outline-0;
    background-color: #e9f8f9;
  }
}
</style>
