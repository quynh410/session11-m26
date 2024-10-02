<template>
  <div>
    <h1>Bai 9</h1>
    <p>Count: {{ count }}</p>
  </div>
</template>

<script setup>
import { ref, onMounted, onUnmounted } from "vue";
const count = ref(0);
let timerId;
onMounted(() => {
  timerId = setInterval(() => {
    count.value++;
  }, 1000);
});
onUnmounted(() => {
  clearInterval(timerId);
});
</script>
