<!-- Ejemplo de reactividad -->

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


</script>

<!-- template puede renderizar todo el componente html -->
<template>
  <!-- llamamos a lam fiunción que hemops declarado -->
  <h1>Hola {{name}}!</h1>

  <h2>{{ counter }}</h2>
  <button @click="increment">Aumentar</button>



</template>

<style>
  h1 {
    color: red;
  }
</style>