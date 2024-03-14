<script setup>
// import { ref } from 'vue'

// let count = ref(0)

// const submitHandler = (e) => {
//   e.preventDefault()
//   alert('valid credentials')
// }

// const incrementCounter = () => count.value++
// const decrementCounter = () => count.value--

const showMessage = (message) => alert(message)
</script>

<template>
  <section style="font-size: 55px">
    <!-- <h1>Count: {{ count }}</h1>
    <button @:click="incrementCounter">Increment</button>
    <button @:click="decrementCounter">Decrement</button> -->

    <!-- <form @submit="submitHandler">
      <input type="text" placeholder="please enter your name" />
      <input type="email" placeholder="Please enter email" />
      <button type="submit">Submit</button>
    </form> -->

    <button @click="showMessage('This is my message')">Show message</button>
  </section>
</template>
