<!-- Propiedades computadas o calculadas -->

<!-- añadir setup a la etiqueta script -->
<script setup> 

// importamos el computed
import { ref, computed } from "vue";

//interpolación de texto
const name = 'Vue dinámico';

// cambiamos la variable por un ref y q se renderice
const counter = ref(0)
const arrayCounter = ref([]);



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

// el computed siempre recibe una funcion de flecha y tiene que retornar algo
const classCounter = computed(() => { 
  if(counter.value === 0) {
    return 'zero'
  }

  if(counter.value > 0) {
    return 'positive'
  }

  if(counter.value < 0) {
    return 'negative'
  }
})

const addCounter = () => { 
  arrayCounter.value.push(counter.value);
}

const blockNumber = computed(() => {
    const number = arrayCounter.value.find((num) => num === counter.value);
    return number || number === 0;
});

</script>

<!-- template puede renderizar todo el componente html -->
<template>

  <!-- llamamos a lam fiunción que hemops declarado -->
  <div class="container">

    <h1>Hola {{name}}!</h1>
  
     <!-- clases dinamicaS -->
    <h2 :class="classCounter">
      {{ counter }}
    </h2>
    <div class="d-flex">
      <button class="btn btn-success mx-1" @click="increment">Aumentar</button>
  
      <button class="btn btn-danger mx-1" @click="decrecent">Disminuir</button>
  
      <button class="btn btn-info mx-1" @click="reset">Reset</button>
      <button class="btn btn-secondary mx-1" @click="addCounter" :disabled="blockNumber">Add</button>

  </div>
  
  
  <h3>lista de valores</h3>
  <ul>

 
    <li v-for="(numbers) in arrayCounter" :key="numbers">
      {{ numbers }}
    </li>
  </ul>
  </div>




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
.zero {
  color: peru;
}
</style>