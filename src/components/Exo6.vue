<script setup>

import { ref } from 'vue';

const name = ref('');
const submitted = ref(false);
function handleSubmit() {
    if (name.value) {
        submitted.value = true;
    } else {
        submitted.value = false;
    }
}
</script>

<template>
    <form @submit.prevent="handleSubmit">
        <input v-model="name" placeholder="Votre nom">
        <button type="submit">Envoyer</button>
    </form>
    <p v-if="submitted && name">Merci {{ name }}</p>
    <p v-else-if="submitted && !name"></p>
    <p v-else class="defaut">Le nom est requis</p>



</template>


<style scoped>


.defaut {
    color:red;
    background-color: rgb(181, 190, 12);
}
</style>