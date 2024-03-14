<template>
  <!-- <h1 :class="$style['m-class']">Using module css with $ syntax (kebab-case)</h1> -->
  <h1 :class="myClasses.sClass">Using module css with $ syntax (camelCase)</h1>
</template>

<style module="myClasses">
.m-class {
  background: firebrick;
  color: white;
}

.sClass {
  background: gray;
  color: blue;
}
</style>
