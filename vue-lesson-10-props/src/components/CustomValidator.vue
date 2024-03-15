<script setup>
defineProps({
  name: {
    type: String,
    validator: (propValue) =>
      ["Alex", "John", "Chris", "Luigi"].includes(propValue),
  },

  age: {
    type: Number,
    validator: (propValue) =>
      propValue >= 18 && propValue <= 30 ? true : false,
  },
  password: {
    type: String,
    validator: (propValue) => propValue.length >= 8 && true,
  },
});
</script>

<template>
  <h1>Name: {{ name }}</h1>
  <h1>Age: {{ age }}</h1>
  <h1>Password: {{ password }}</h1>
</template>
