<template>
  <div>
    <h1>Bài 2</h1>
    <p>Count: {{ count }}</p>
    <button @click="incrementCount">Counter</button>
  </div>
</template>

<script setup>
import { onUpdated, ref } from 'vue';

// Khởi tạo biến count với ref
const count = ref(0);

// Phương thức tăng giá trị count
const incrementCount = () => {
  count.value++;
};

onUpdated(()=>{
    console.log("Du lieu da thay doi");
    
})
</script>
