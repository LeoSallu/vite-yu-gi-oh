<script>

export default {

}
</script>
<template>
    <!-- Header  -->
    <header>
        <div id="logo" class="d-flex align-items-center">
            <div class="img">
                    <img src="../../../public/img/logo.webp" alt="logo">
            </div>
            <div class="text">
                <h1>Yu-gi-oh Api</h1>
            </div>
        </div>
    </header>
    <!-- /Header  -->
</template>
<style lang="scss" scoped>
@use '../../assets-styles/main.scss' as *;

#logo{
    .img {
        width: 140px;
        height: 100px;
        img{
            width: 100%;
            display: block;
        }
    }
}
</style>