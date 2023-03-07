<template>
  <h1 v-bind:class="selector">
    HOLA {{ miNombre }} y tendré {{ miEdad }}
  </h1>
</template>


<!-- Codigo Javascript ,con setup evitamos exportar-->

<script setup>
  const miNombre="Ramon"
  const miEdad=28
  const miColor="color:green;font-size:3em"
  const selector="azul"
</script>


<!-- scoped solo afecta a este elemento -->
<!-- Quito estilo h1 para prevalezca el estilo de directiva de arriba -->
<style scoped>
.azul{
  color:blue;
}
</style>