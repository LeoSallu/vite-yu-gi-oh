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
}
}
</script>
<template>
    <main>
        <!-- Dropdown menu  -->
        <DropdownApp />
        <!-- Card List  -->
        <CardList />
    </main>
</template>
<style lang="scss" scoped>
@use '../../assets-styles/main.scss' as *;
@use '../../assets-styles/_partials/variable.scss' as *;

main {
    background-color: $primary;
}
</style>