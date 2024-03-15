<template>
  <div>
    <h1 :ref="myRefFunc">This is the initial value</h1>
  </div>
</template>

<script setup>
const myRefFunc = (el) => {
  console.log(el.textContent);
  el.textContent = "Text Changed";
  el.style.color = "crimson";
};
</script>

<style scoped></style>
