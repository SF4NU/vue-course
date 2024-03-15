<template>
  <div v-if="showFriends">
    <RenderFriends />
  </div>
  <button @click="toggleFriends">Toggle friend list</button>
</template>

<script setup>
import { ref, defineAsyncComponent } from "vue";
const RenderFriends = defineAsyncComponent(() => import("./RenderFriends.vue"));

let showFriends = ref(false);

const toggleFriends = () => {
  showFriends.value = !showFriends.value;
};
</script>

<style scoped></style>
