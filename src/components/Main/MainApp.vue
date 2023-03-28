<script>
import DropdownApp from './DropdownApp.vue';
import CardList from './CardList.vue';
import { store } from '../../store';
export default {
    components:{
        DropdownApp,
        CardList
    },
    data() {
        return {
            store,
        }
    },
        methods: {
            handleSelect(){
                this.$emit('select');
            }
}}
</script>
<template>
    <main>
        <div class="container p-4">
        <!-- Dropdown menu  -->
            <DropdownApp @select="handleSelect"/>
        <!-- Card List  -->
            <CardList />
        </div>
    </main>
</template>
<style lang="scss" scoped>
@use '../../assets-styles/main.scss' as *;
@use '../../assets-styles/_partials/variable.scss' as *;

main {
    background-color: $primary;
}
</style>