<script>
import { store } from '../../store';
    export default{
        name: 'Card',
        props:{
            img:String,
            name:String,
            type:String
        },
        data(){
            return
            store
        }
    }
</script>
<template>
    <div class="card" style="width: 18rem;">
        <img :src="img" class="card-img-top" alt="...">
        <div class="card-body">
            <h5 class="card-title">{{name}}</h5>
            <p class="card-text">{{type}}</p>
        </div>
    </div>
</template>