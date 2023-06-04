<script setup>
import Text from "../Text/text.vue";

const props = defineProps({
  perPersonResult: {
    type: Number,
    default: 0,
  },
  tipAmount: {
    type: Number,
    default: 0,
  },
});

console.log({ props: props.tipAmount });
</script>

<template>
  <div class="container">
    <div class="mb-10">
      <div class="tipItem mb-12">
        <div>
          <Text style="color: #fff">Tip Amount</Text>
          <Text>/ person</Text>
        </div>
        <div>
          <h1 class="amount">${{ tipAmount.toFixed(2) }}</h1>
        </div>
      </div>
      <div class="tipItem">
        <div>
          <Text style="color: #fff">Total Amount</Text>
          <Text>/ person</Text>
        </div>
        <div>
          <h1 class="amount">${{ perPersonResult.toFixed(2) }}</h1>
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
