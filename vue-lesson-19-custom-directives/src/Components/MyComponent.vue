<template>
  <div v-format1-div:orange>Using simple custom directive</div>
  <div v-format-div:red>Using simple custom directive</div>
  <div v-format-div:blue>Using simple custom directive</div>
  <div v-format-div:pink>Using simple custom directive</div>
  <div v-format-div>Using simple custom directive</div>
</template>

<script setup>
const vFormatDiv1 = {
  mounted: (el, binding) => {
    el.style.fontSize = binding.value + "px";
    el.style.fontSize = `${binding.value}rem`;
    el.style.border = `${binding.value}px solid green`;

    console.log(binding.arg);
    el.style.fontSize = "5rem";

    switch (binding.arg) {
      case "orange":
        el.style.color = "orange";
        break;
      case "red":
        el.style.color = "red";
        break;
      case "blue":
        el.style.color = "blue";
        break;
      case "pink":
        el.style.color = "pink";
        break;
      default:
        el.style.color = "black";
    }
  },
};

const vFormatDiv = (el) => (el.style.fontSize = "5rem"); //forma corta
</script>

<style scoped></style>
