<script setup>
import { ref, reactive } from 'vue'

let count = ref(0)
let username = ref('')
let usersList = ref(['Mario', 'Luigi', 'Peach'])
let userInfo = ref({ name: 'Alex', age: 20, location: ['NYC', 'idk'], isMarried: false })

let friends = reactive([ref('Jordan'), ref('Alex'), ref('Luigi')])
</script>

<template>
  <h1>Count: {{ count }}</h1>
  <button @click="count++">+</button>
  <button @click="count--">-</button>
  <section>
    <h1>1 {{ friends[0] }}</h1>
    <h1>2 {{ friends[1] }}</h1>
    <h1>3 {{ friends[2] }}</h1>

    <button @click="friends[0] = '🤝'">Hand shake</button>
    <button @click="friends[1] = '🤝'">Hand shake</button>
    <button @click="friends[2] = '🤝'">Hand shake</button>

    <h1>Name: {{ userInfo.name }}</h1>
    <h1>Age: {{ userInfo.age }}</h1>
    <h1>Location: {{ userInfo.location[0] }}</h1>
    <h1>Married?: {{ userInfo.isMarried }}</h1>

    <button @click="userInfo.name = 'Luigi'">Change name</button>
    <button @click="userInfo.age = 40">Change age</button>
    <button @click="userInfo.location = ['Earth', 'meh']">Change location</button>
    <button @click="userInfo.isMarried = true">Change status</button>

    <h1>Users list: {{ usersList }}</h1>
    <button @click="usersList.push('Bowser')">Add User</button>
    <h1>username: {{ username }}</h1>
    <button @click="username = 'Jordan'"></button>
  </section>
</template>
