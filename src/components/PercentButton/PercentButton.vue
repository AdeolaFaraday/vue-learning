<script setup>
defineProps({
  text: {
    type: String,
    required: true,
  },
});
</script>
<template>
  <div class="buttonContainer">{{ text }}</div>
</template>

<style scoped>
@tailwind base;
@tailwind components;
@tailwind utilities;

@layer components {
  .buttonContainer {
    @apply h-10 text-white text-xl font-semibold rounded flex justify-center items-center;
    font-family: "Dosis", sans-serif;
    background-color: #245953;
    width: calc(34.5% - 1rem);
  }
}
</style>
