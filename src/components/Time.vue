<template>
  <div>
    <h1>Time : {{ time }}</h1>
  </div>
</template>

<script setup>
import {
  onBeforeMount,
  onBeforeUnmount,
  onBeforeUpdate,
  onMounted,
  onUnmounted,
  onUpdated,
  ref,
} from "vue";
const time = ref(0);
let timerId;
// giai doan mounting
onBeforeMount(() => {
  console.log("components be fore mount");
});
onMounted(() => {
  console.log("components mounted");
  timerId = setInterval(() => {
    time.value++;
  }, 1000);
});
// giai doan updating
onBeforeUpdate(() => {
  console.log("components be fore update");
});
onUpdated(() => {
  console.log("components updated");
});
// giai doan UnMount
onBeforeUnmount(() => {
  console.log("components be fore unmount");
});
onUnmounted(() => {
  console.log("components unmounted");
  clearInterval(timerId);
});
</script>
