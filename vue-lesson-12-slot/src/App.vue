<script setup>
import SlotComponent from "./Components/SlotComponent.vue";
import FallbackContent from "./Components/FallbackContent.vue";
import NamedSlotComponent from "./Components/NamedSlotComponent.vue";
import DefaultSlot from "./Components/DefaultSlot.vue";
</script>

<template>
  <SlotComponent>
    <h1>Content 1</h1>
    <h1>Content 12</h1>
  </SlotComponent>
  <hr />
  <FallbackContent>
    Fallback wont work because i am providing content inside the component
  </FallbackContent>

  <hr />

  <NamedSlotComponent>
    <template v-slot:one> <h1>This content will go to slot 1</h1></template>
    <template v-slot:two> <h1>This content will go to slot 2</h1></template>
  </NamedSlotComponent>

  <DefaultSlot>
    <template #default>
      <h1>This is some default content</h1>
    </template>
  </DefaultSlot>
</template>

<style scoped></style>
