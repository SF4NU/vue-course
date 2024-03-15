<script setup>
import { ref } from "vue";
const firstName = ref("Luigi");
const lastName = ref("Mario");
const number = ref(7);
import PropsComponent from "./components/PropsComponent.vue";
import DynamicPropsComponent from "./components/DynamicPropsComponent.vue";
import ChangePropsValue from "./components/ChangePropsValue.vue";
import PropValidation from "./components/PropValidation.vue";
import ComplexProps from "./components/ComplexProps.vue";
import CustomValidator from "./components/CustomValidator.vue";
</script>

<template>
  <PropsComponent name="Chris" />
  <hr />
  <DynamicPropsComponent :firstName="firstName" :lastName="lastName" />
  <hr />
  <ChangePropsValue :number="number" />
  <hr />
  <PropValidation fullName="Bowser" :age="20" />
  <hr />
  <ComplexProps
    :friends="['Alex', 'John', 'Chris', 'Luigi']"
    :userInfo="{ name: 'alex', age: 20, location: ['NYC', 'idk'] }" />
  <hr />
  <CustomValidator name="Peach" :age="20" password="passwordssss" />
</template>

<style>
body {
  height: 1500px;
}
</style>
