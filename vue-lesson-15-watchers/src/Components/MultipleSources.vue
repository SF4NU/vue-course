<template>
  <div>
    <h1>{{ username }}</h1>
    <h1>{{ counter }}</h1>

    <button @click="username = 'Mickey'">Change Name</button>
    <button @click="counter++">Increment Counter</button>
  </div>
</template>

<script setup>
import { ref, watch } from "vue";

const username = ref("Alex");
const counter = ref(0);

watch([username, counter], (newVal, oldVal) => {
  console.log("New Value", newVal);
  console.log("Old Value", oldVal);
});
</script>

<style scoped></style>
