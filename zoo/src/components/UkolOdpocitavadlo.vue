<script setup>
import {ref} from "vue";
const cislo = ref(10);


const odpocet = setInterval(() => {
cislo.value--;
 
    
    if (cislo.value <= 0) {
        cislo.value = "HOTOVO!"
        clearInterval(odpocet);
    }
}, 1000);


</script>

<template>
    <h2>Odpočet</h2>
    <p>{{ cislo }}</p>
</template>

<style scoped>

p {
    
        color:black
    }

</style>