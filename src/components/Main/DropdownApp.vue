<script>
import { store } from '../../store';
export default {
    data() {
        return {
            store
        }
    }
}
</script>
<template>
    <select class="form-select w-25" v-model="store.cardType" @select.prevent="$emit('handleSelect')">
        <option selected>Select your type</option>
        <option v-for="(type,index) in store.cardType" :value="index">{{type.archetype_name}}</option>
    </select>
</template>