<script setup>
import { ref } from "vue";

let people = ref(["Alex", "Jordan", "Nick"]);
const books = ref([
  {
    id: 1,
    title: "To Kill a Mockingbird",
    author: "Harper Lee",
    genre: "Fiction",
    publicationYear: 1960,
  },
  {
    id: 2,
    title: "1984",
    author: "George Orwell",
    genre: "Dystopian",
    publicationYear: 1949,
  },
  {
    id: 3,
    title: "Pride and Prejudice",
    author: "Jane Austen",
    genre: "Romance",
    publicationYear: 1813,
  },
]);

let moreBooks = ref([
  [
    "The Secret Garden",
    "Alice's Adventures in Wonderland",
    "The Catcher in the Rye",
  ],
  ["Lord of the Flies", "The Great Gatsby", "To Kill a Mockingbird"],
  ["Brave New World", "Moby-Dick", "War and Peace"],
]);

let games = ref({
  game1: {
    title: "The Legend of Zelda: Breath of the Wild",
    genre: "Action-adventure",
    platform: "Nintendo Switch",
    releaseYear: 2017,
  },
  game2: {
    title: "The Witcher 3: Wild Hunt",
    genre: "Action role-playing",
    platform: "Various",
    releaseYear: 2015,
  },
  game3: {
    title: "Red Dead Redemption 2",
    genre: "Action-adventure",
    platform: "PlayStation 4, Xbox One, PC, Stadia",
    releaseYear: 2018,
  },
});

let moreComplexObj = ref({
  game1: {
    title: "Space Explorer",
    genre: "Sci-Fi",
    platform: "PC",
    releaseDate: "2023-05-20",
  },
  game2: {
    title: "Fantasy Quest",
    genre: "Fantasy",
    platform: "PlayStation",
    releaseDate: "2023-07-10",
  },
  movie1: {
    title: "Inception",
    director: "Christopher Nolan",
    genre: "Sci-Fi",
    releaseDate: "2010-07-16",
  },
  movie2: {
    title: "The Shawshank Redemption",
    director: "Frank Darabont",
    genre: "Drama",
    releaseDate: "1994-09-23",
  },
  book1: {
    title: "Dune",
    author: "Frank Herbert",
    genre: "Science Fiction",
    publicationYear: 1965,
  },
  book2: {
    title: "To Kill a Mockingbird",
    author: "Harper Lee",
    genre: "Fiction",
    publicationYear: 1960,
  },
});
</script>

<template>
  <p v-for="(person, index) in people" :key="index">{{ person }}</p>

  <ul
    v-for="({ id, title, author, genre, publicationYear }, index) in books"
    :key="index">
    <li>ID: {{ id }}</li>
    <li>Title: {{ title }}</li>
    <li>Author: {{ author }}</li>
    <li>Genres: {{ genre }}</li>
    <li>Publication Year: {{ publicationYear }}</li>
  </ul>

  <ul v-for="(book, index) in moreBooks" :key="index">
    <li v-for="(b, i) in book" :key="i">{{ b }}</li>
  </ul>

  <ul v-for="(value, keys, index) in games" :key="value">
    {{
      index
    }}
    -
    {{
      keys
    }}
    -
    {{
      value
    }}
  </ul>

  <ul v-for="(game, index) in moreComplexObj" :key="index">
    <li>{{ game }}</li>
    <br />

    <li v-for="(property, i) in game" :key="i">{{ property }}</li>
  </ul>

  <ul
    v-for="({ title, author, genre, releaseDate }, index) in moreComplexObj"
    :key="index">
    <li>{{ title }}</li>
    <li>{{ author }}</li>
    <li>{{ genre }}</li>
    <li>{{ releaseDate }}</li>
  </ul>

  <ul v-for="number in 5" :key="number">
    <li>{{ number }}</li>
  </ul>
</template>
