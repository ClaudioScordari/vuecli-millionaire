<!-- 
    Come importare un componente:
    1. si importa questo nel file App.vue nella prima riga dello script;
    2. si dichiara il componente nella chiave components;
    3. utilizzo del componente tramite un self closing tag con il nome del componente.
-->

<script>
import Main from './components/Main.vue';

export default {
    data() {
        return {
            
        }
    },
    components: {
        Main
    }
}


</script>

<!-- --------------------------------------------------------------------------------- -->

<template>
    <Main />
</template>

<!-- --------------------------------------------------------------------------------- -->

<style scoped>

</style>
