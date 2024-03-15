<template>
  <div>
    <h1>Using fetch</h1>
    <button @click="fetchData">Fetch Data</button>
    <button @click="postData">Post Data</button>
    <div>
      <h2>Data from api:</h2>
      <pre>{{ data }}</pre>
    </div>
  </div>
</template>

<script setup>
import { ref } from "vue";
import axios from "axios";

const data = ref(null);

// const fetchData = () => {
//   fetch("https://go-fiber-prova-production.up.railway.app/tasks")
//     .then((res) => {
//       if (!res.ok) {
//         throw new Error(`HTTP ERROR STATUS: ${res.status}`);
//       }
//       return res.json();
//     })
//     .then((resData) => {
//       data.value = resData;
//     })
//     .catch((error) => {
//       console.error(`Error fetching data: ${error}`);
//     });
// };
const fetchData = async () => {
  try {
    const res = await axios.get(
      "https://go-fiber-prova-production.up.railway.app/tasks"
    );

    data.value = res.data;
  } catch (error) {
    console.error();
  }
};
const postData = async () => {
  try {
    const res = await axios.post(
      "https://go-fiber-prova-production.up.railway.app/tasks",
      {
        description: "Prova prova prosadeqvaaaasafdaaaaa",
        completed: false,
        deadline: "17-05",
      }
    );
  } catch (error) {
    console.error();
  }
};
</script>

<style scoped></style>
