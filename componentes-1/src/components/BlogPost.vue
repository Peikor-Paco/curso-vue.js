<script setup>
// Props y Multiples prop
// definimos los props lo qiue son los elementos dinamicos en un array de 
defineProps(['title', 'content']);

</script>


<template>
  
<div class="card">
    <div class="card-body">
        <!-- usamos la interpolación -->
        <h5 class="card-title">{{ title }}</h5>
        <p class="card-text">{{ content }}</p>
    </div>
</div>
</template>

<style scoped>

</style>