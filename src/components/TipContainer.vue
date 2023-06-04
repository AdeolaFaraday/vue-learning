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
    @apply flex-col lg:flex-row lg:w-3/5 w-full lg:rounded-2xl rounded-t-3xl lg:p-10 p-6 flex justify-stretch gap-8;
    background-color: #fff;
    box-shadow: 25px 25px 50px 25px rgb(0 0 0 / 0.1);
    @media screen(lg) {
      box-shadow: 0px 25px 50px -12px rgb(0 0 0 / 0.2);
    }
  }
  .tipContainerItem {
    @apply w-full lg:w-1/2;
  }
}
</style>
