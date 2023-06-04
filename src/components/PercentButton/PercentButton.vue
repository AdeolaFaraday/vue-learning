<script setup>
defineProps({
  text: {
    type: String,
    required: true,
  },
});
defineEmits(["percent-click"]);
</script>
<template>
  <div @click="$emit('percent-click', text)" class="buttonContainer">
    {{ text + "%" }}
  </div>
</template>

<style scoped>
@tailwind base;
@tailwind components;
@tailwind utilities;

@layer components {
  .buttonContainer {
    @apply h-10 text-white text-xl font-semibold rounded flex justify-center items-center cursor-pointer;
    font-family: "Space Mono", sans-serif;
    background-color: #245953;
    width: calc(50% - 1rem);
    @media screen(lg) {
      width: calc(33.4% - 1rem);
    }
  }
}
</style>
