<!-- 
    Come importare un componente:
    1. si importa questo nel file App.vue nella prima riga dello script;
    2. si dichiara il componente nella chiave components;
    3. utilizzo del componente tramite un self closing tag con il nome del componente.
-->

<script>
// 1. import AppQualcosa from './components/AppQualcosa.vue';

export default {
    data() {
        return {
            
        }
    },
    // 2. Dichiarazione dei componenti
    components: {
        // AppQualcosa
    }
}


</script>

<!-- --------------------------------------------------------------------------------- -->

<template>
    <div>
        <!-- 3. <AppQualcosa/> -->


    </div>
</template>

<!-- --------------------------------------------------------------------------------- -->

<style scoped>

</style>
