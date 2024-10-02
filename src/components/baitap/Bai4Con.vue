<template>
  <div>
   
  </div>
</template>

<script setup>
import { onUpdated, defineProps } from "vue";
const props = defineProps({
  age: Number,
});

onUpdated(() => {
  console.log();
  alert(`Tuoi da doi ${props.age}`)
});
</script>
