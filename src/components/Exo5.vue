<script setup>

import { ref } from 'vue';
const compteur = ref(0);

const incrementer = () => {
    compteur.value++;
};

const decrementer = () => {
    compteur.value--;
};

const reinitialiser = () => {
    compteur.value = 0;
};

</script>

<template>
    <div class="compteur-container">

        <p class="compteur-valeur">{{ compteur }}</p>
        <div class="boutons">
            <button @click="incrementer"> ➕ Incrémenter</button>
            <button @click="decrementer"> ➖ Décrémenter</button>
            <button @click="reinitialiser"> 🔁 Réinitialiser</button>
        </div>
    </div>


</template>


<style scoped></style>