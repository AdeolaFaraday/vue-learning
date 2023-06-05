<script setup>
import { ref } from "vue";

const props = defineProps({
  icon: {
    type: String,
  },
});
const emit = defineEmits(["input-change"]);
const text = ref(null);
const handleInputChange = () => {
  emit("input-change", text.value);
};

const getImgUrl = (iconValue) => {
  return new URL("/src/assets/" + iconValue, import.meta.url);
};
</script>
<template>
  <div class="relative">
    <img class="absolute h-4 w-3 bottom-4 left-3" :src="getImgUrl(icon)" />
    <input
      type="text"
      v-model="text"
      @input="handleInputChange"
      placeholder="0"
      class="input"
    />
  </div>
</template>

<style scoped>
@tailwind base;
@tailwind components;
@tailwind utilities;

@layer components {
  .input {
    @apply h-12 px-6 rounded w-full focus:outline-0 text-right text-2xl font-semibold;
    font-family: "Space Mono", sans-serif;
    background-color: #e9f8f9;
  }
}
</style>
