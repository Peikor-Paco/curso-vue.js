<!-- single file component logica, estructura y estilos en un solo fichero -->

<!-- añadir setup a la etiqueta script -->
<script setup> 
//interpolación de texto
const name = 'Vue dinámico';
</script>

<!-- template puede renderizar todo el componente html -->
<template>
  <!-- llamamos el contenido de la constante {{name}} -->
  <h1>Hola {{name}}!</h1>
</template>

<style>
  h1 {
    color: red;
  }
</style>