<!-- v-if v-for juntos (mucho cuidado ?) 
 v-for + v-if + template

-->

<!-- añadir setup a la etiqueta script -->
<script setup> 
//interpolación de texto
const name = 'Vue dinámico';



// array
const arrayFrutas = [
    {
        name: "Manzana",
        price: "$1.00",
        description: "Una manzana",
        stock: 0,
    },
    {
        name: "Pera",
        price: "$2.00",
        description: "Una pera",
        stock: 10,
    },
    {
        name: "Naranja",
        price: "$3.00",
        description: "Una naranja",
        stock: 20,
    },
  ]

</script>

<!-- template puede renderizar todo el componente html -->
<template>
  <!-- llamamos el contenido de la constante {{name}} -->
  <h1>Hola {{name}}!</h1>
  <!-- v-if tiene mayor peso que el v-for, vue primero lee el v-if y luego el v-for -->
  <ul>
    <li 
    v-for="item in arrayFrutas" 
    :key="item.name">
      <span v-if="item.stock > 0" >
        {{ item.name }} - 
        {{ item.price }}
      </span>
    </li>
  </ul>
  <p>Utilizamos el template para poner el v-for</p>
  <ul>
    <template v-for="item in arrayFrutas" 
    :key="item.name">
      <li v-if="item.stock > 0" >
          {{ item.name }} - 
          {{ item.price }}
      </li>
    </template>
  </ul>
</template>

<style>
  h1 {
    color: red;
  }
</style>