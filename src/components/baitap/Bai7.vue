<template>
  <div>
    <h1>Bai 7</h1>
    <input type="text" v-model="inputValue">
  </div>
</template>

<script setup>
import { onUpdated, ref } from "vue";

    const inputValue = ref("")
    onUpdated(()=>{
        document.title = inputValue.value
    })
</script>

<style>

</style>