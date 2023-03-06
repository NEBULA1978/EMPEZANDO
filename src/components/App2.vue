<template>
  <div>
    <h1>HOLA {{ miNombre }} y tendré {{ miEdad }}</h1>
    <label>Edad 1:</label>
    <input type="number" v-model="miEdad" />
    <!-- <label>Edad 2:</label>
    <input type="number" v-model="miEdad" /> -->
  </div>
</template>

<script setup>
const miNombre = "Ramon"
let miEdad = 28
</script>

<style scoped>
h1 {
  color: red;
}
</style>
