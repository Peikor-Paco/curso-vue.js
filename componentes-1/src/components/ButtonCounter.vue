<script setup>

import { ref } from "vue";

const counter = ref(0)

const increment = () => {
  counter.value ++;
}


</script>


<template>
  <button class="btn btn-success mx-1" @click="increment">Aumentar {{ counter }}</button>
</template>

<style scoped>

</style>