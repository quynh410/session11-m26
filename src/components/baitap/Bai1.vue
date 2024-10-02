<template>
  <div>
    <h1>Bai 1</h1>
  </div>
</template>

<script setup>
import { onBeforeMount, onMounted } from "vue";

onBeforeMount(() => {
  console.log("components be fore mount");
  
});
onMounted(() => {
  console.log("components mounted");
});
</script>

<style>

</style>