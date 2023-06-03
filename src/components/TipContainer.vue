<script setup>
import Calculation from "./CalculationSection/calculation.vue";
import ResultContainer from "./ResultContainer/ResultContainer.vue";
</script>
<template>
  <div class="tipContainer">
    <div class="tipContainerItem">
      <Calculation />
    </div>
    <div class="tipContainerItem">
      <ResultContainer />
    </div>
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
    @apply w-3/5 rounded-2xl p-10 flex justify-stretch gap-8;
    background-color: #fff;
  }
  .tipContainerItem {
    @apply w-1/2;
  }
}
</style>
