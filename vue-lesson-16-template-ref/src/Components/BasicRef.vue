<template>
  <div>
    <input type="text" placeholder="Enter your name" ref="myRef" />
  </div>
</template>

<script setup>
import { onMounted, ref } from "vue";
const myRef = ref("Luigi");

onMounted(() => {
  console.log(myRef.value);
  myRef.value.focus();
  myRef.value.value = "something else";
});
</script>

<style scoped></style>
