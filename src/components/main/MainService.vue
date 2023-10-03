<script>
export default {
    name: 'MainService'
}
</script>

<template>
    <div class="row my-5">
        <div class="col-3 position-relative">
            <div class="img-wrapper">
                <a href="#" class="img position-absolute camion"></a>
            </div>
            <div class="text">
                <h5 class="text-capitalize m-0">free delivery</h5>
                <p class="text-capitalize m-0">free shipping on all order</p>

            </div>
        </div>
        <div class="col-3">
            <div class="img-wrapper">
                <a href="#" class="img position-absolute bag "></a>
            </div>
            <div class="text">
                <h5 class="text-capitalize m-0">money return</h5>
                <p class="text-capitalize m-0">back guarantee in 7 days</p>

            </div>
        </div>
        <div class="col-3">
            <div class="img-wrapper">
                <a href="#" class="img position-absolute discount"> </a>
            </div>
            <div class="text">
                <h5 class="text-capitalize m-0">member discount</h5>
                <p class="text-capitalize m-0">on every order over $130.00</p>

            </div>
        </div>
        <div class="col-3">
            <div class="img-wrapper">
                <a href="#" class="img position-absolute money"></a>

            </div>
            <div class="text">
                <h5 class="text-capitalize m-0">return policy</h5>
                <p class="text-capitalize m-0">support 24 hours a day </p>

            </div>
        </div>

    </div>
</template>

<style lang="scss" scoped>
@use '../../assets/scss/partials/variables' as *;

.row {
    padding: 0.5rem;


    .col-3 {
        &:not(:last-child) {
            border-right: 2px solid rgba(128, 128, 128, 0.2);
        }

        .img-wrapper {
            .img {
                width: 70px;
                height: 50px;
                background-repeat: no-repeat;

                &.camion {
                    background-image: url(../../assets/img/service-icon.png);
                    background-position: 0px -112px;
                }

                &.bag {
                    background-image: url(../../assets/img/service-icon.png);
                    background-position: 0px -335px;
                }

                &.discount {
                    background-image: url(../../assets/img/service-icon.png);
                    background-position: 0px -562px;
                }

                &.money {
                    background-image: url(../../assets/img/service-icon.png);
                    background-position: 0px -787px;
                }
            }
        }
    }

    .text {
        margin-left: 5rem;
    }
}
</style>