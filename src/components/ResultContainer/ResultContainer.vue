<script setup>
import Text from "../Text/text.vue";
</script>

<template>
  <div class="container">
    <div>
      <div class="tipItem mb-12">
        <div>
          <Text style="color: #fff">Tip Amount</Text>
          <Text>/ person</Text>
        </div>
        <div>
          <h1 class="amount">$0.00</h1>
        </div>
      </div>
      <div class="tipItem">
        <div>
          <Text style="color: #fff">Total Amount</Text>
          <Text>/ person</Text>
        </div>
        <div>
          <h1 class="amount">$0.00</h1>
        </div>
      </div>
    </div>
    <div class="button"><h3>RESET</h3></div>
  </div>
</template>

<style scoped>
@tailwind base;
@tailwind components;
@tailwind utilities;

@layer components {
  .container {
    @apply h-full w-full rounded-2xl p-8 flex flex-col justify-between;
    background-color: #245953;
  }
  .tipItem {
    @apply flex justify-between items-center;
  }
  .amount {
    @apply text-5xl font-semibold;
    font-family: "Space Mono", sans-serif;
    color: #00dfa2;
  }
  .button {
    @apply w-full h-11 rounded flex justify-center items-center font-semibold cursor-pointer;
    font-size: 1.5rem;
    font-family: "Roboto Mono", sans-serif;
    background-color: #00dfa2;
  }
}
</style>
