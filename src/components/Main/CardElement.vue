<script>
import { store } from '../../store';
    export default{
        name: 'Card',
        loaded:false,
        props:{
            img:String,
            name:String,
            type:String
        },
        beforeMount(){
            this.loaded=false
        },
        data(){
            return
            store
        },
        mounted(){
            this.loaded=true
        }
    }
</script>
<template>
    <div class="card g-2 mt-2" style="width: 18rem;">
        <img :src="img" class="card-img-top" alt="card">
        <div class="card-body">
            <h5 class="card-title">{{name}}</h5>
            <p class="card-text">{{type}}</p>
        </div>
    </div>
</template>