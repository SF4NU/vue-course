<template>
  <section>
    <h2 class="g-1">Another global style</h2>
    <h2 class="g-2">Another local style</h2>
  </section>
</template>

<style>
.g-1 {
  background: fuchsia;
  color: white;
}
</style>

<style scoped>
.g-2 {
  background: black;
  color: white;
}
</style>
