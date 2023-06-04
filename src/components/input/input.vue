<script setup>
import { ref } from "vue";

const emit = defineEmits(["input-change"]);
const text = ref(null);
const handleInputChange = () => {
  emit("input-change", text.value);
};
</script>
<template>
  <div>
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
    @apply h-12 px-6 rounded w-full focus:outline-0 text-right;
    background-color: #e9f8f9;
  }
}
</style>
