<script setup>

// importamos el componente boton contador
import ButtonCounter from './components/ButtonCounter.vue';

</script>

<template>
<div class="container ">
  <div class="d-flex align-items-center flex-column">

    <h1>APP</h1>
    <br>
    <div class="d-flex">
      <!-- llamamos al bototn-->
      <ButtonCounter></ButtonCounter>
    </div>
  </div>
</div>
</template>

<style scoped>

</style>
