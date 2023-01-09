<!-- Práctica
Agrega un botón para disminuir el contador.
Agrega un botón para resetear el contador.
Pinta el contador en rojo cuando el valor sea menor a cero.
Pinta el contador en verde cuando el valor sea mayor a cero. -->

<!-- añadir setup a la etiqueta script -->
<script setup> 

import { ref } from "vue";

//interpolación de texto
const name = 'Vue dinámico';

// cambiamos la variable por un ref y q se renderice
const counter = ref(0)

// incremento de cantidad
const increment = () => {
  // la variable se convierte en un objeto hay que entrar en el valor del objeto
  counter.value ++;
}

const decrecent = () => {
  counter.value --;
}

const reset = () => {
  counter.value=0

}


</script>

<!-- template puede renderizar todo el componente html -->
<template>

  <!-- llamamos a lam fiunción que hemops declarado -->
  <h1>Hola {{name}}!</h1>

  

  <h2 v-if="counter <= 0" style="color:red">{{ counter }}</h2>
  <h2 v-else style="color:green" >{{ counter }}</h2>


 <!-- clases dinamicaS -->
  <h2 :class="counter >= 0 ? 'positive' : 'negative'">
        {{ counter }}
  </h2>

  <button @click="increment">Aumentar</button>

  <button @click="decrecent">Disminuir</button>

  <button @click="reset">Reset</button>




</template>

<style>
  h1 {
    color: red;
  }

  .negative {
    color: red;
}

.positive {
    color: green;
}
</style>