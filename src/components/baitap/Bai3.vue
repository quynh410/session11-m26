<template>
  <div>
    <h1>Bai 3</h1>
    <p>Current Company: {{ input }}</p>
    <p>Age: {{ age }}</p>
    <button @click="handleRandom">Random</button>
  </div>
</template>

<script setup>
import { onBeforeUpdate, onUpdated, ref } from "vue";

const input = ref("Rikkei Academy");
const age = ref(1);

const handleRandom = () => {
  const companies = ["Rikkei Academy", "Rikkei Fukuoka","Rikkei Education"];
  input.value = companies[Math.floor(Math.random() * companies.length)];
  age.value = Math.floor(Math.random() * 10) + 1; 
};

onBeforeUpdate(() => {
  console.log("before updated");
});

onUpdated(() => {
  console.log("Component updated");
});
</script>

<style></style>
