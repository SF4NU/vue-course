<script setup>
import { ref, computed } from 'vue'
const number = ref(5)

const squaredNumber = computed(() => {
  return number.value * number.value
})

const firstName = ref('Luigi')
const lastName = ref('Bowser')

const fullName = computed(() => firstName.value + ' ' + lastName.value)

const counter = ref(0)

const squaredCounter = computed(() => counter.value ** 2)

const incrementCounter = () => {
  counter.value++
}
</script>

<template>
  <h1>Counter: {{ counter }}</h1>
  <h1>Squared Counter: {{ squaredCounter }}</h1>
  <button @click="incrementCounter">Increment counter</button>
  <!-- <h1>Full name: {{ fullName }}</h1> -->

  <!-- <h1>Original number: {{ number }}</h1>
  <h1>Squared number: {{ squaredNumber }}</h1> -->
</template>
