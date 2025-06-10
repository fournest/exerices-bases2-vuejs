<script setup>

import { ref } from 'vue';

const produits = [
    {nom : 'Chaise', prix: 30},
    {nom : 'Banc',  prix: 50},
    {nom : 'table', prix: 80}
]

</script>

<template>
<ul>
    <li v-for="(produit, index) in produits" :key="index" > {{ produit.nom }} : {{ produit.prix }}€</li>
    
</ul>


</template>


<style scoped>


</style>