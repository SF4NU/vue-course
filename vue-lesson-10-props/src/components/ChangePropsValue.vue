<script setup>
import { ref } from "vue";
const number = defineProps(["number"]);
</script>

<template>
  <h1>{{ number.number }}</h1>
</template>
