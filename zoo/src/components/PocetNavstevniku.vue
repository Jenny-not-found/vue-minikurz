<script setup>
import {ref} from "vue";
const pocet = ref(100);

setInterval(() => {
    //kdykoliv budeme chtit cist nebo menit hodnotu reaktivni promenne, tak musime jit pres vlastnost value.
    pocet.value = Math.floor(Math.random() * 10000);
}, 2000);
</script>

<template>
    <!-- double mustache rika ze zde se ma vypast nejaka reaktivni hodnota -->
    <!-- double mustache nemuzete pouzit v atributu elementu -->
    <p>Počet návštěvníků: {{ pocet }}</p>
</template>

<style scoped>

</style>