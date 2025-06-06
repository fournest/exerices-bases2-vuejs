<script setup>

import { ref } from 'vue';


const name = ref('');
const email = ref('');
const islooged = ref(false);



</script>

<template>
    <form  @submit.prevent="islooged = !islooged">
        <label for="name">Votre nom : </label>
        <input type="text" id="name" v-model="name" required />
        <label for="email">Votre email: </label>
        <input type="email" id="email" v-model="email" required />
        <button type="submit">S'inscrire!</button>

        <p v-if="islooged">Bienvenue, {{ name }}! Votre email {{ email }} a été enregistré.</p>
    </form>

</template>


<style scoped></style>