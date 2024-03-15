<script setup>
import LifeCycleComponent from "./Components/LifeCycleComponent.vue";
import { ref } from "vue";
const showHide = ref(true);
</script>

<template>
  <LifeCycleComponent v-if="showHide" />
  <button @click="showHide = !showHide">show/hide</button>
</template>

<style scoped></style>
