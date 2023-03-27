<script>
import { store } from '../../store';
    export default{
        name: 'Card',
        loaded: false,
        props:{
            img:String,
            name:String,
            type:String
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
        </div>
    </div>
</template>