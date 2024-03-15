<template>
  <div>
    <MyComponent ref="myRef" />
  </div>
</template>

<script setup>
import MyComponent from "./MyComponent.vue";

import { onMounted, ref } from "vue";

const myRef = ref(null);

onMounted(() => {
  console.log(myRef.value);
});
</script>

<style scoped></style>
