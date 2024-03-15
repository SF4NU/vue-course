<template>
  <div>
    <h1>Count: {{ counter.count }}</h1>
    <button @click="counter.increment">+</button>
    <button @click="counter.decrement">-</button>
  </div>
</template>

<script setup>
import { useCounter } from "../shared/useCounter";
const counter = useCounter();
</script>

<style scoped></style>
