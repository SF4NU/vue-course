<template>
  <div>
    <h1>{{ state.username }}</h1>
    <button @click="state.username = 'Alex'">Change name</button>
  </div>
</template>

<script setup>
import { reactive, watch } from "vue";
const state = reactive({ username: "Chris" });

watch(
  () => state.username,
  (newValue, oldValue) => {
    console.log("newValue", newValue);
    console.log("oldValue", oldValue);
  }
);
</script>

<style scoped></style>
