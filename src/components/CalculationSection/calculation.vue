<script setup>
import PercentButton from "../PercentButton/PercentButton.vue";
import Text from "../Text/text.vue";
import Input from "../input/input.vue";
</script>
<template>
  <div class="container">
    <div class="sectionContainer">
      <Text class="m-2">Bills</Text>
      <Input />
    </div>
    <div class="sectionContainer">
      <Text class="mb-4">Select Tip%</Text>
      <div class="percentContainer">
        <PercentButton
          v-for="item in ['5%', '10%', '25%', '30%', '40%']"
          :text="item"
        />
      </div>
    </div>
    <div>
      <Text class="m-2">Number of people</Text>
      <Input />
    </div>
  </div>
</template>

<style scoped>
@tailwind base;
@tailwind components;
@tailwind utilities;

@layer components {
  .container {
    @apply w-full;
  }
  .percentContainer {
    @apply flex flex-row flex-wrap gap-4;
  }
  .sectionContainer {
    @apply mb-12;
  }
}
</style>
