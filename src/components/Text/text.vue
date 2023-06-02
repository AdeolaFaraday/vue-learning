<script setup>
defineProps({
  style: {
    type: Object,
  },
});
</script>
<template>
  <div>
    <h1 :style="style" class="text">
      <slot></slot>
    </h1>
  </div>
</template>

<style scoped>
.text {
  font-family: "Roboto Mono", sans-serif;
  font-size: 1rem;
  font-weight: 500;
  color: #7b8fa1;
}
</style>
