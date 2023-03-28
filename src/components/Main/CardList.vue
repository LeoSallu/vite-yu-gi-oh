<script>
import CardElement from './CardElement.vue';
import { store } from '../../store';
export default {
   
    components: { 
        CardElement
    },
    data(){
        return{
            store,
            loaded:false
        }
    },
    mounted(){
            this.loaded=true
    }
}
</script>
<template>
    <div class="container-fluid">
        <div class="row">
            <div id="black_bg" class="p-3">
                <h5>Found {{store.cardsFound}} cards</h5>
            </div>
            <div v-for="card in (store.cards).slice(0,100)" class="col-3">
                <!-- Card  -->
                <CardElement 
                :img="card.card_images[0].image_url"
                :name="card.name"
                :type="card.type"
                :price="card.card_prices[0].cardmarket_price"
                />
                <!-- /Card  -->
            </div>
            <!-- Animazione Caricamento  -->
            <!-- <LoadingAnimation v-show="loaded=false"/> -->
            <!-- /Animazione Caricamento -->
        </div>
    </div>
</template>
<style lang="scss" scoped>
@use '../../assets-styles/_partials/variable.scss' as *;

.container-fluid {
    background-color: white;

    #black_bg {
        background-color: black;

        h5 {
            color: white;
        }
    }
}
.card-body{
    background-color: $primary ;
}
</style>