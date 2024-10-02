<template>
  <div>
    <h1>Bai 6</h1>
    <p>Count : {{ count }}</p>
    <button @click="handleClick">Increment</button>
  </div>
</template>

<script setup>
import { onMounted, onUpdated, ref } from "vue";
const count = ref(0);
const handleClick = () => {
  count.value++;
};
onUpdated(() => {
  document.title = `Count : ${count.value}`;
});
onMounted(() => {
  document.title = `Count : ${count.value}`;
});
</script>

<style></style>
