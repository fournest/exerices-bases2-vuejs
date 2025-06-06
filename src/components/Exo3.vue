<script setup>

import { ref } from 'vue';



const actif = ref(false);



</script>

<template>


    <button @click="actif = !actif">Activez/Desactivez</button>

    <div>
        <p :class="actif ? 'actif' : 'inactif'">{{ actif? 'Utilisateur actif' : 'Utilisateur inactif' }}</p>
      
    </div>


</template>


<style scoped>
.actif {

    color: lightcoral;
}

.inactif {

    color: brown;
}
</style>