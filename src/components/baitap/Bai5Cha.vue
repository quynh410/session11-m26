<template>
  <div>
    <h1>Bai 5 - Parent Component</h1>
    <div>
      <Bai5Con v-if="isShow" />
      <button @click="handleShow">Toggle</button>
    </div>
  </div>
</template>

<script setup>
import { ref } from "vue";
import Bai5Con from "./Bai5Con.vue";
const isShow = ref(false);

const handleShow = () => {
  isShow.value = !isShow.value;
};
</script>

<style></style>
