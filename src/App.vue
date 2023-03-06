<template>
  <h1>HOLA {{ miNombre }} y tendré {{ miEdad }}</h1>
</template>


<!-- Codigo Javascript ,con setup evitamos exportar-->

<script setup>
  const miNombre="Ramon"
  const miEdad=28
</script>


<!-- scoped solo afecta a este elemento -->
<style scoped>
  h1{
    color: red;
  }
</style>