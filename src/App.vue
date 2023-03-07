<template>
<button @click="decremento">-</button>
<span>{{ contador }}</span>
<button @click="incremento">+</button>
</template>


<!-- Codigo Javascript ,con setup evitamos exportar-->

<script setup>
  const contador=0;
  const decremento = ()=>{
    contador--;
  }
  const incremento = ()=>{
    contador++;
  }

</script>


<!-- scoped solo afecta a este elemento -->
<!-- Quito estilo h1 para prevalezca el estilo de directiva de arriba -->
<style scoped>
.azul{
  color:blue;
}
</style>