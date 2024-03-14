<script setup>
import { reactive } from 'vue'

let initialState = reactive({ val: { count: 0 }, users: ['mike', 'jordan'] })

const changeUser = () => {
  initialState.users[0] = 'Chris'
  initialState.users[1] = 'Tom'
}
const addOneUser = () => {
  initialState.users.push('Timmy')
}
</script>

<template>
  <section>
    <h1>Current count: {{ initialState.val.count }}</h1>
    <h1>Users: {{ initialState.users }}</h1>

    <button @click="initialState.val.count += 10">Add 10</button>
    <button @click="changeUser()">Change User</button>
    <button @click="addOneUser()">Add one more</button>

    <!-- <h1>Count: {{ initialState.count }}</h1> -->
    <!-- <button @click="initialState.count++">+</button>
    <button @click="initialState.count--">-</button> -->
  </section>
</template>
