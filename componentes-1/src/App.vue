<script setup>

// importamos el componente boton contador
import ButtonCounter from './components/ButtonCounter.vue';
import BlogPost from './components/BlogPost.vue';

</script>

<template>
<div class="container ">
  <div class="d-flex align-items-center flex-column">

    <h1>APP</h1>
    <br>
    <div class="d-flex">
      <!-- llamamos al bototn-->
      <ButtonCounter />
    </div>

    <hr />

    <BlogPost 
      title="Post 1"
      content="Contenido 1"
    />
    <BlogPost 
      title="Post 2"
      content="Contenido 2"
    />
    <BlogPost 
      title="Post 3"
      content="Contenido 3"
    />
  </div>
</div>
</template>

<style scoped>

</style>
