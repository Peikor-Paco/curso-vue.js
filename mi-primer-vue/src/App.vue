<!-- single file component logica, estructura y estilos en un solo fichero -->

<!-- añadir setup a la etiqueta script -->
<script setup> 
//interpolación de texto
const name = 'Vue dinámico';
// v-bind permite comunicar le script y el template en los atributos
const styleColor = "color: blue";

//Expresiones de javascript
// Array
const arrayColores = ["blue","yellow"]

//Booleano
const activo = true;


// v-for iterar sobre una lista de elementos. 
const arrayFrutas = ["🍎", "🍌", "🍉", "🍓", "🍒"];

</script>

<!-- template puede renderizar todo el componente html -->
<template>
  <!-- llamamos el contenido de la constante {{name}} -->
  <h1>Hola {{name}}!</h1>

  <h1>Hola {{name.toUpperCase()}}!</h1>
  <h2 style="color: blue">Tengo un color azul</h2>
  <!-- añadimos el v-bind: para llamar -->
  <h2 v-bind:style="styleColor">Tengo un color azul con v-bind variable</h2>
  <!-- podemos dejar solo los dos punto : -->
  <h2 :style="styleColor">Tengo un color azul con dos puntos variable</h2>


  <h2>{{ arrayColores }}</h2>

  <h2>{{ activo ? "Soy activo" : "No soy activo" }}</h2>
  <!-- v-if -->
  <p v-if="activo">Estoy activo</p>
  <p v-if="!activo">Estoy inactivo</p>

  <!-- v-if v-else siempre tiene que estar seguido al v-if -->

  <p v-if="activo">Estoy activo con else</p>
  <p v-else>Estoy inactivo con else</p>


  <!-- v-if v-els-if -->

  <p v-if="activo === true">Estoy activo con else if</p>
  <p v-else-if="activo === false">Estoy inactivo con else if</p>
  <p v-else>Estoy indeciso con else if </p>

  <!-- v-show oculta atraves de css con el display none -->
  <p v-show="activo">Estoy visible con v-show</p>


  <!-- v-for -->
  <ul>
    <li v-for="(fruta, index) in arrayFrutas" :key="index">
      {{ index + 1 }} {{ fruta }}
    </li>
  </ul>
</template>

<style>
  h1 {
    color: red;
  }
</style>