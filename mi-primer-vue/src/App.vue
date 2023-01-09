<!-- v-for array de objetos -->

<!-- añadir setup a la etiqueta script -->
<script setup> 
//interpolación de texto
const name = 'Vue dinámico';

const arrayFrutas = [
        {
            name: "Manzana",
            price: "$1.00",
            description: "Una manzana",
        },
        {
            name: "Pera",
            price: "$2.00",
            description: "Una pera",
        },
        {
            name: "Naranja",
            price: "$3.00",
            description: "Una naranja",
        },
    ];

</script>

<!-- template puede renderizar todo el componente html -->
<template>
  <!-- llamamos el contenido de la constante {{name}} -->
  <h1>Hola {{name}}!</h1>

  <!-- v-for -->
  <ul>
    <li v-for="(fruta) in arrayFrutas" :key="fruta.name">
      {{ fruta.name }} - 
      {{ fruta.price }} - 
      {{ fruta.description }}
    </li>
  </ul>


</template>

<style>
  h1 {
    color: red;
  }
</style>