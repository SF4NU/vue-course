<template>
  <div>
    <h4>Injecting Array</h4>
    <ul v-for="(friend, index) in friendsList" :key="index">
      <li>{{ friend }}</li>
    </ul>
    <ul v-for="(game, index) in games" :key="index">
      <li>{{ game }}</li>
    </ul>
    <ul
      v-for="({ title, genre, platform, releaseDate }, index) in moreGames"
      :key="index">
      <li>{{ title }}</li>
      <li>{{ genre }}</li>
      <li>{{ platform }}</li>
      <li>{{ releaseDate }}</li>
    </ul>
  </div>
</template>

<script setup>
import { inject } from "vue";
const friendsList = inject("friends");
const games = inject("games");
const moreGames = inject("moreGames");
</script>

<style scoped></style>
