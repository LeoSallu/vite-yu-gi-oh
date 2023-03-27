<!-- My Js -->
<script>
import HeaderApp from './components/Header/HeaderApp.vue';
import MainApp from './components/Main/MainApp.vue';
    export default{
    components: {
        MainApp,
        HeaderApp
    }
}
</script>
<!-- My Html -->
<template>
    <HeaderApp />
    <MainApp />
</template>
<!-- My Scss -->
<style lang="scss" scoped>
@use './assets-styles/main.scss' as *;
</style>