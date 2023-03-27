<script>
import CardElement from './CardElement.vue';
import { store } from '../../store';
export default {
   
    components: { 
        CardElement 
    },
    data(){
        return{
            store
        }
    }
}
</script>
<template>
    <div class="container p-5">
        <div id="black_bg" class="row">
            <h5>Found 39 cards</h5>
        </div>
        <div class="row">
            <div v-show="loaded=true" v-for="card in store.cards" class="col">
                <!-- Card  -->
                <CardElement 
                :img="card.card_images[0].image_url"
                :name="card.name"
                :type="card.type"
                />
                <!-- /Card  -->
            </div>
        </div>
    </div>
</template>
<style lang="scss" scoped>
@use '../../assets-styles/main.scss' as *;
@use '../../assets-styles/_partials/variable.scss' as *;

.container {
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