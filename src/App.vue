<!-- My Js -->
<script>
// Import Risorse 
import axios from 'axios';
import { store } from './store';
import HeaderApp from './components/Header/HeaderApp.vue';
import MainApp from './components/Main/MainApp.vue';
    export default{
        // Componenti 
    components: {
        MainApp,
        HeaderApp
    },
    data(){
        return{
            store
        }
        
    },
    created(){
            // API 
            axios.get('https://db.ygoprodeck.com/api/v7/cardinfo.php')
                .then((response) => {
                    this.store.cards = response.data.data;
                })
        }
}
</script>
<!-- My Html -->
<template>
    <HeaderApp />
    <MainApp />
</template>
<!-- My Scss -->
<style lang="scss" scoped>
@use './assets-styles/main.scss' as *;
</style>