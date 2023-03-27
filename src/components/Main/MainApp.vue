<script>
import DropdownApp from './DropdownApp.vue';
import CardList from './CardList.vue';
export default {
    components:{
        DropdownApp,
        CardList
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
    height: 90vh;
}
</style>