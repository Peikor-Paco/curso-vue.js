<!-- Evento Click (v-on) o @ -->

<!-- añadir setup a la etiqueta script -->
<script setup> 

//interpolación de texto
const name = 'Vue dinámico';

//método - methods

const handleClick = () => {
  console.log("me distes click");
}


</script>

<!-- template puede renderizar todo el componente html -->
<template>
  <!-- llamamos a lam fiunción que hemops declarado -->
  <h1>Hola {{name}}!</h1>
  <button v-on:click="handleClick">Activame</button>
  <button @click="handleClick">Activame 2</button>
</template>

<style>
  h1 {
    color: red;
  }
</style>