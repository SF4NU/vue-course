<template>
  <div>
    <h1>{{ message }}</h1>
    <input v-model="inputText" placeholder="Type something..." type="text" />
  </div>
</template>

<script setup>
import { ref, watch } from "vue";
const message = ref("hello, vue!");
const inputText = ref("aaaa");

watch(inputText, (newValue, oldValue) => {
  message.value = `You typed: ${newValue}`;
  console.log(newValue);
  console.log(oldValue);
});
</script>

<style scoped></style>
