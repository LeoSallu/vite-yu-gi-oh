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
    methods:{
        select(){
            // API 
            axios.get('https://db.ygoprodeck.com/api/v7/cardinfo.php')
                .then((response) => {
                    this.store.cards = response.data.data;
                    this.store.cardsFound = response.data.data.length;
                }),
                axios.get('https://db.ygoprodeck.com/api/v7/archetypes.php')
                .then((response) => {
                    this.store.cardType = response.data.archetype_name;
                })
        }
    },
    created(){
           this.select();
        }
}


</script>
<!-- My Html -->
<template>
    <HeaderApp />
    <MainApp/>
</template>
<!-- My Scss -->
<style lang="scss" scoped>
@use './assets-styles/main.scss' as *;
</style>