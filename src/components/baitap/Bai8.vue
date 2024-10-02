<template>
  <div>
    <h1>Bai 8</h1>
    <p>Chiều rộng cửa sổ: {{ windowWidth }}px</p>
  </div>
</template>

<script setup>
import { ref, onMounted, onUnmounted } from 'vue';
const windowWidth = ref(window.innerWidth);
const updateWidth = () => {
  windowWidth.value = window.innerWidth;
};
onMounted(() => {
  window.addEventListener('resize', updateWidth);
});
onUnmounted(() => {
  window.removeEventListener('resize', updateWidth);
});
</script>
