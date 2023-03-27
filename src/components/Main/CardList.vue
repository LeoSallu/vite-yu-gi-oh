<script>
export default {

}
</script>
<template>
    <div class="container p-5">
        <div id="black_bg" class="row">
            <h5>Found 39 cards</h5>
        </div>
        <div class="row">
            <div class="col">
                <!-- Card  -->
                <div class="card" style="width: 18rem;">
                    <img src="..." class="card-img-top" alt="...">
                    <div class="card-body">
                        <h5 class="card-title">Card title</h5>
                        <p class="card-text">Some quick example text to build on the card title and make up the bulk of the
                            card's content.</p>
                        <a href="#" class="btn btn-primary">Go somewhere</a>
                    </div>
                </div>
                <!-- /Card  -->
            </div>
        </div>
    </div>
</template>
<style lang="scss" scoped>
@use '../../assets-styles/main.scss' as *;
@use '../../assets-styles/_partials/variable.scss' as *;

.container {
    background-color: white;

    #black_bg {
        background-color: black;

        h5 {
            color: white;
        }
    }
}
</style>