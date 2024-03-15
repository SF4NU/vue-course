<script setup>
import SchoolComponent from "./Components/SchoolComponent.vue";
import PracticeComponent from "./Components/PracticeComponent.vue";
import { provide } from "vue";

provide("studentName", "Alex");
provide("studentAge", 20);
provide("studentLocation", ["Earth", "IDK"]);

//Provide array
provide("friends", ["Alex", "Jordan", "John", "Mickey"]);

//Provide objects
provide("games", {
  id: 1,
  title: "Epic Adventure Game",
  genre: ["Action", "Adventure", "RPG"],
  platform: ["PC", "PlayStation", "Xbox", "Nintendo Switch"],
  releaseDate: "2022-03-15",
  developer: {
    name: "Awesome Game Studios",
    location: "San Francisco, CA",
    teamSize: 50,
  },
});

//Provide Array of Objects
provide("moreGames", [
  {
    title: "Space Explorer",
    genre: "Sci-Fi",
    platform: "PC",
    releaseDate: "2023-05-20",
  },
  {
    title: "Fantasy Quest",
    genre: "Fantasy",
    platform: "PlayStation",
    releaseDate: "2023-07-10",
  },
  {
    title: "Inception",
    director: "Christopher Nolan",
    genre: "Sci-Fi",
    releaseDate: "2010-07-16",
  },
  {
    title: "The Shawshank Redemption",
    director: "Frank Darabont",
    genre: "Drama",
    releaseDate: "1994-09-23",
  },
]);
</script>

<template>
  <SchoolComponent />
  <hr />
  <PracticeComponent />
</template>

<style scoped></style>
