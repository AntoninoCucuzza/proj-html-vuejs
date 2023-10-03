<script>
export default {
    name: 'SpecialCategory',

}
</script>
<template>
    <div class="row my-5 flex-column align-items-center ">
        <h1 class=" text-center m-0">Special Category</h1>
        <div class="splitter my-3"></div>
        <div class="row">
            <div class="col-4 ">
                <div class="overlay-wrapper">
                    <div class="overlay position-absolute">
                        <h5>Battlefield 3</h5>
                        <a href="#">Shop Now</a>
                    </div>
                    <img class="img-fluid" src="../../assets/img/category-image-02-446x550_t.jpg" alt="">
                </div>
            </div>
            <div class="col-4 ">
                <div class="overlay-wrapper">
                    <div class="overlay position-absolute">
                        <h5>Pubg</h5>
                        <a href="#">Shop Now</a>
                    </div>
                    <img class="img-fluid" src="../../assets/img/category-image-01-446x550_t.jpg" alt="">
                </div>
            </div>
            <div class="col-4 ">
                <div class="overlay-wrapper">
                    <div class="overlay position-absolute">
                        <h5>Jump Force</h5>
                        <a href="#">Shop Now</a>
                    </div>
                    <img class="img-fluid" src="../../assets/img/category-image-03-446x550_t.jpg" alt="">
                </div>
            </div>

        </div>

    </div>
</template>

<style lang="scss" scoped>
@use '../../assets/scss/partials/variables' as *;
@use '../../assets/scss/partials/splitter' as *;

.row {
    padding: 0;

    .col-4 {
        .overlay-wrapper {
            position: relative;
            padding: 0;
            margin: 0;
            overflow: hidden;


            .overlay {
                bottom: 0;
                left: 0;
                background-color: rgba(0, 0, 0, 0.5);
                width: 100%;
                padding: 0.5rem;
                padding-top: 1.5rem;
                transition: all 0.3s;

                a {
                    text-decoration: underline;
                    color: $gh_warning;
                }
            }

            &:hover .overlay {
                background-color: $gh_violet_darker;
            }
        }



    }
}
</style>