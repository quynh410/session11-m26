<template>
  <div>
    <h1>Bai 10</h1>
    <b>Thoi gian hien tai : {{ time }}</b>
  </div>
</template>

<script setup>
import { onBeforeUnmount, onMounted, ref } from "vue";
let timerId;
const formatDate = (date) => {
  const today = new Date(date);
  // lay ra gio
  const hours = today.getHours().toString().padStart(2, 0);
  // lay ra phut
  const minutes = today.getMinutes().toString().padStart(2, 0);
  // lay ra giay
  const seconds = today.getSeconds().toString().padStart(2, 0);
  // format thoi gian
  return `${hours}:${minutes}:${seconds}`;
};
const time = ref(formatDate(new Date()));
onMounted(() => {
  timerId = setInterval(() => {
    time.value = formatDate(new Date());
  }, 1000);
});
onBeforeUnmount(() => {
  clearInterval(timerId);
});
</script>

<style></style>
