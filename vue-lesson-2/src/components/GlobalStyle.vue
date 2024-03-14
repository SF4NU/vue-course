<template>
  <section>
    <h1 class="text-red">global styling</h1>
    <p class="local">Trying local scope in this component</p>
  </section>
</template>
<!--Global style, per farlo diventare local metti attributo scoped-->
<style>
.text-red {
  color: red;
}
</style>
