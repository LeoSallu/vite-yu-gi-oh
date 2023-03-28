<script>
import { store } from '../../store';
export default{
    data(){
        return{
            store
        }
    }
}
</script>
<template>
    <div class="dropdown-center my-3">
            <button class="btn btn-light dropdown-toggle" type="button" data-bs-toggle="dropdown">
               Scegli la tua carta
            </button>
            <ul class="dropdown-menu">
                <li v-for="card in (store.cards).slice(20,40)"><a class="dropdown-item" href="#">{{card.name}}</a></li>
            </ul>
        </div>
</template>