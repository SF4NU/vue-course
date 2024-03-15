<template>
  <div>
    <h1>Student component</h1>
    <h1>{{ studentName }}</h1>
    <h1>{{ studentAge }}</h1>
    <h1>{{ studentLocation }}</h1>
  </div>
</template>

<script setup>
import { inject } from "vue";

const studentName = inject("studentName");
const studentAge = inject("studentAge");
const studentLocation = inject("studentLocation");
</script>

<style lang="css" scoped></style>
