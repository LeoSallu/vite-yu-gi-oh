<script>
import { store } from '../../store';
    export default{
        name: 'Card',
        loaded: false,
        props:{
            img:String,
            name:String,
            type:String,
            price:String
        },        
        data(){
            return{
                store
            }
        }
    }
</script>
<template>
    <div v-show="loaded=true" class="card text-bg-primary my-2" style="width: 18rem;">
        <img :src="img" class="card-img-top" alt="card">
        <div class="card-body p-4">
            <h5 class="card-title text-light">{{name}}</h5>
            <small class="card-text">{{type}}</small>
            <h6 class="card-text" id="cardmarket">CardMarket price is <span>{{price}}€</span></h6>
        </div>
    </div>
</template>
<style lang="scss" scoped>
#cardmarket{
    color: #022169;
    span{
    color: white;
}
}
</style>