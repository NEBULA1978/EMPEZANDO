<template>
<button @click="decremento">-</button>
<span :class="miColor">{{ contador }}</span>
<button @click="incremento">+</button>
<div v-if="contador<0">Escribe una cantidad mayor de 0</div>
<div v-else-if="contador>=5">Escribe una cantidad menior de 5</div>
<div v-show="comprobacion">No esta permitodo el número 0</div>
<img :src="imagen1" alt="imagen">
</template>

<!-- El .value solo utilizamos en script no en template -->
<!-- Codigo Javascript ,con setup evitamos exportar-->

<script setup>
import {ref,computed} from "vue";
import { valores } from "./datos.js"
const imagen1 = valores[0].web

// import imagen2 from "./assets/logo.svg"
// Es un string no un variable ponemos entre comillas
const miColor=ref("azul")
  // Creamos variable reactiva
  const contador=ref(0);
  const decremento = ()=>{
    contador.value--;
    // Hacemos referencia a una variable de tipo reactivo
    if (contador.value<0){
      miColor.value="rojo"
    }
  }
  const incremento = ()=>{
    contador.value++;
    if (contador.value > 5) {
    miColor.value = "verde"
  }

  }
  const comprobacion=computed(()=>{
    return contador.value === 0;

    
  })

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