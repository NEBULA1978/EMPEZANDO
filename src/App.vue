<template>
<button @click="decremento">-</button>
<span>{{ contador }}</span>
<button @click="incremento">+</button>
</template>


<!-- Codigo Javascript ,con setup evitamos exportar-->

<script setup>
import {ref} from "vue";
  // Creamos variable reactiva
  const contador=ref(0);
  const decremento = ()=>{
    contador.value--;
  }
  const incremento = ()=>{
    contador.value++;
  }

</script>


<!-- scoped solo afecta a este elemento -->
<!-- Quito estilo h1 para prevalezca el estilo de directiva de arriba -->
<style scoped>
span{
  padding: 0 5px;
}
</style>