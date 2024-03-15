<template>
  <div>
    <h3 v-for="(friend, index) in friends" :key="index">{{ friend }}</h3>
  </div>
</template>

<script setup>
import { ref } from "vue";

const friends = ref(["Mario", "Luigi", "Peach", "Bowser"]);
</script>

<style scoped></style>
