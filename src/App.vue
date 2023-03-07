<template>
<button @click="decremento">-</button>
<span :class="miColor">{{ contador }}</span>
<button @click="incremento">+</button>
</template>


<!-- Codigo Javascript ,con setup evitamos exportar-->

<script setup>
import {ref} from "vue";
// Es un string no un variable ponemos entre comillas
const miColor=ref("azul")
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
.rojo{
  color: red;
}
.verde{
  color: green;
}
.azul{
  color: blue;
}
</style>