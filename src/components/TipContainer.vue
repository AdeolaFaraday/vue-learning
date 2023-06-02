<script setup>
import Calculation from "./CalculationSection/calculation.vue";
</script>
<template>
  <div class="tipContainer">
    <div class="tipContainerItem">
      <Calculation />
    </div>
    <div class="tipContainerItem"></div>
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
  .tipContainer {
    @apply w-3/5 rounded-2xl p-10;
    background-color: #fff;
  }
  .tipContainerItem {
    @apply w-1/2;
  }
}
</style>
