<script setup>
import ComponentEvent from "./Components/ComponentEvent.vue";
import FromComponent from "./Components/FromComponent.vue";
import { ref } from "vue";

let count = ref(0);

const formHandler = (username, email, password) => {
  console.log("username", username);
  console.log("email", email);
  console.log("password", password);
};
</script>

<template>
  <h1>{{ count }}</h1>
  <ComponentEvent @incrementCounter="count++" />
  <hr />
  <FromComponent @userInfo="formHandler" />
</template>

<style scoped></style>
