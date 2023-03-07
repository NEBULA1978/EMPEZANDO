<template>
  <h1 :class="selector">
    HOLA {{ miNombre }} y tendré {{ miEdad }}
  </h1>
  <!-- <button v-on:click="">Aceptar</button> -->
  <button @click="saludar">Aceptar</button>
</template>


<!-- Codigo Javascript ,con setup evitamos exportar-->

<script setup>
  const miNombre="Ramon"
  const miEdad=28
  const miColor="color:green;font-size:3em"
  const selector="azul"
  // FUNCION
  const saludar=()=>{
    console.log("Hola")
  }
</script>


<!-- scoped solo afecta a este elemento -->
<!-- Quito estilo h1 para prevalezca el estilo de directiva de arriba -->
<style scoped>
.azul{
  color:blue;
}
</style>