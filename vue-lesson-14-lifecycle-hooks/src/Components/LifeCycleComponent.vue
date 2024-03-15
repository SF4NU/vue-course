<template>
  <div>
    <h1>{{ message }}</h1>
    <h2>{{ count }}</h2>
    <button @click="count++">Update Message</button>
  </div>
</template>

<script setup>
import {
  ref,
  onBeforeMount,
  onMounted,
  onBeforeUpdate,
  onUpdated,
  onBeforeUnmount,
  onUnmounted,
} from "vue";

const message = ref("Hello, Vue!");
let count = ref(0);

//Lifecycle hooks

onBeforeMount(() => {
  console.log("Component is about to be mounted");
});

onMounted(() => {
  console.log("Component has been mounted");
});

onBeforeUpdate(() => {
  console.log("Component is about to be updated");
});

onUpdated(() => {
  console.log("Component has been updated");
});

onBeforeUnmount(() => {
  console.log("Components is about to be unmounted");
});

onUnmounted(() => {
  console.log("Component has been unmounted");
});
</script>

<style scoped></style>
