<script setup>
import {reactive, ref} from "vue";

let annee = ref(2023);
let fruits = reactive(["pomme", "poire", "banane"]);
</script>

<template>
  <ul>
    <li v-for="fruit in fruits" :key="fruit">{{ fruit }}</li>
  </ul>
  <p>
    {{ annee }} -
    <slot>Hello !</slot>
  </p>
</template>

<style scoped>
p {
  background-color: yellow;
  text-transform: uppercase;
}
</style>
