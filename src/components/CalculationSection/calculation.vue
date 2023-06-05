<script setup>
import PercentButton from "../PercentButton/PercentButton.vue";
import Text from "../Text/text.vue";
import Input from "../input/input.vue";

const emit = defineEmits(["bill-input-change", "people-no-change"]);
const handleBillsChange = (value) => {
  emit("bill-input-change", value);
};
const handlePeopleChange = (value) => {
  emit("people-no-change", value);
};

const handlePercentClick = (value) => {
  emit("percent-click", value);
};
</script>
<template>
  <div class="container">
    <div class="sectionContainer">
      <Text class="m-2">Bills</Text>
      <Input @input-change="handleBillsChange" icon="icon-dollar.svg" />
    </div>
    <div class="sectionContainer">
      <Text class="mb-4">Select Tip%</Text>
      <div class="percentContainer">
        <PercentButton
          v-for="item in ['5', '10', '15', '25', '50']"
          :text="item"
          @percent-click="handlePercentClick"
        />
      </div>
    </div>
    <div>
      <Text class="m-2">Number of people</Text>
      <Input icon="icon-person.svg" @input-change="handlePeopleChange" />
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
