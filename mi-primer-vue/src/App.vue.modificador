<!-- Evento Click (v-on) o @ -->

<!-- añadir setup a la etiqueta script -->
<script setup> 

//interpolación de texto
const name = 'Vue dinámico';

//método - methods

const handleClick = (message) => {
  console.log(message);
}


</script>

<!-- template puede renderizar todo el componente html -->
<template>
  <!-- llamamos a lam fiunción que hemops declarado -->
  <h1>Hola {{name}}!</h1>
   <!-- eventos de click en raton -->
  <button v-on:click.right.prevent="handleClick('texto Right')">Activame right</button>
  <button @click="handleClick('Texto Left')">Activame left</button>
  <button @click.middle="handleClick('Texto Middle')">Activame middle</button>
</template>

<style>
  h1 {
    color: red;
  }
</style>