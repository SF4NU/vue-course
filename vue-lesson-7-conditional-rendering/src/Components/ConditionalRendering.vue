<script setup>
import { ref } from "vue";

let isVisible = ref();

const isTrue = false;
const isFalse = false;

let isLoggedIn = ref(true);
let username = "Luigi";
let showDetails = ref(isLoggedIn);

const isActive = ref(true);

let password = ref(false);
</script>

<template>
  <h1 v-if="password.length > 8">Strong password</h1>
  <h1 v-else-if="password.length < 8">Weak password</h1>
  <h1 v-else>Please enter your password</h1>

  <div v-if="isActive">
    <h1>My Blog Post</h1>
    <p>
      Lorem ipsum dolor sit amet consectetur adipisicing elit. Nobis explicabo
      minus magni voluptatum libero! Unde magni quidem dolor optio obcaecati.
      Quas sapiente expedita animi aliquam numquam deleniti autem reprehenderit
      minima.
    </p>
  </div>

  <button @click="isActive = !isActive">Toggle Post</button>

  <div>
    <h1 v-if="isLoggedIn">Welcome, {{ username }}</h1>
    <h1 v-else>Please log in</h1>

    <div v-show="showDetails">
      <h3>You're now able to modify...</h3>
    </div>

    <p v-if="isTrue">This will show if true</p>
    <p v-else-if="isFalse">This will show if isFalse is true</p>
    <p v-else>This will show if neither isTrue nor ifFalse is true</p>

    <p v-show="isVisible">
      This paragraph will be s hown or hidden based on the val ue of isVisible
    </p>
    <button @click="isVisible = !isVisible"></button>
  </div>
</template>
