<script setup>
// Props y Multiples prop
// definimos los props lo qiue son los elementos dinamicos en un array de 
defineProps(['title', 'content', 'colorText']);

</script>


<template>
  
<div class="card">
    <div class="card-body">
        <!-- usamos la interpolación -->
        <!-- usamos las clases -->
        <h5 class="card-title" :class="`text-${colorText}`">{{ title }}</h5>
        <p class="card-text">{{ content }}</p>
    </div>
</div>
</template>

<style scoped>

</style>