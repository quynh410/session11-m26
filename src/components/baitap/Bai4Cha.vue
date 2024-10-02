<template>
  <div>
    <h1>Bai 4 - Parent Component</h1>
    <p>Age: {{ age }}</p>
    <button @click="increaseAge">Increase Age</button>

    <bai-4-con :age="age" ></bai-4-con>
  </div>
</template>

<script setup>
import { ref } from 'vue';
import Bai4Con from './Bai4Con.vue'
const age = ref(0);

const increaseAge = () => {
  age.value += 1;
};
</script>
