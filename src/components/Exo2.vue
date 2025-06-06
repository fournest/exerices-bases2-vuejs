<script setup>

import { ref } from 'vue';


const taches = ref([]);
const nvTache = ref('');
function ajouterTache() {
    if (nvTache.value.trim() !== '') {
        taches.value.push(nvTache.value);
        nvTache.value = '';
    }
}

</script>

<template>

    <textarea name="tache" id="tache" v-model="nvTache"></textarea>
    <button @click="ajouterTache">ajouter une tache</button>

    <ul>
        <li v-for="tache in taches" :key="tache">{{ tache }}</li>
    </ul>


</template>


<style scoped></style>