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
                <h5 class="text-capitalize m-0 title">free delivery</h5>
                <p class="text-capitalize m-0">free shipping on all order</p>

            </div>
        </div>
        <div class="col-3">
            <div class="img-wrapper">
                <a href="#" class="img position-absolute bag "></a>
            </div>
            <div class="text">
                <h5 class="text-capitalize m-0 title">money return</h5>
                <p class="text-capitalize m-0">back guarantee in 7 days</p>

            </div>
        </div>
        <div class="col-3">
            <div class="img-wrapper">
                <a href="#" class="img position-absolute discount"> </a>
            </div>
            <div class="text">
                <h5 class="text-capitalize m-0 title">member discount</h5>
                <p class="text-capitalize m-0">on every order over $130.00</p>

            </div>
        </div>
        <div class="col-3">
            <div class="img-wrapper">
                <a href="#" class="img position-absolute money"></a>

            </div>
            <div class="text">
                <h5 class="text-capitalize m-0 title">return policy</h5>
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
                background-image: url(../../assets/img/service-icon.png);
                background-repeat: no-repeat;

                &.camion {
                    background-position: 0px -112px;

                    &:hover {
                        background-position: 0px 1px;

                    }
                }

                &.bag {
                    background-position: 0px -335px;

                    &:hover {
                        background-position: 0px -222px;

                    }
                }

                &.discount {
                    background-position: 0px -562px;

                    &:hover {
                        background-position: 0px -449px;



                    }

                }

                &.money {
                    background-position: 0px -787px;

                    &:hover {
                        background-position: 0px -674px;

                    }
                }
            }
        }
    }

    .text {
        margin-left: 5rem;
    }
}
</style>