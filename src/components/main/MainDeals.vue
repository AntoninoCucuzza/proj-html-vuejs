<script>
export default {
    name: "MainDeals",
    props: {
        isTrue: { type: Boolean, },
        title: { type: String },
    },

}   
</script>

<template>
    <div class="d-flex flex-column align-items-center wrapper">
        <h1 class="text-capitalize text-center">{{ title }}</h1>
        <div class="splitter"></div>

        <!-- se confermo la condizione nell'elemento padre vedro 4 diverse caselle  -->
        <template v-if="isTrue">
            <div class="wrapeer_container_lg">
                <div class="row">
                    <div class="col-3 text-center">1026 days</div>
                    <div class="col-3 text-center">13 hours</div>
                    <div class="col-3 text-center">24 mins</div>
                    <div class="col-3 text-center">17 secs</div>
                </div>
            </div>
        </template>

        <!-- se falsa nell'elemento padre vedro 3 diverse caselle  -->
        <template v-else>
            <div class="wrapeer_container_sm">
                <div class="row">
                    <div class="col-4 text-center">
                        <a class="active" href="#">Featured</a>
                    </div>
                    <div class="col-4 text-center">
                        <a href="#">New Arrival</a>
                    </div>
                    <div class="col-4 text-center">
                        <a href="#">Best Seller</a>
                    </div>

                </div>
            </div>
        </template>

    </div>
</template>

<style lang="scss" scoped>
@use '../../assets/scss/partials/splitter' as *;
@use '../../assets/scss/partials/variables' as *;


.wrapper {
    .wrapeer_container_lg {
        width: 100%;
        max-width: 600px;
        margin: 1rem auto;

        .col-3 {
            border: 1px solid $gh_gray;
            padding: 0.5rem;
            color: $gh_gray;

        }
    }

    .wrapeer_container_sm {
        width: 100%;
        max-width: 400px;
        margin: 1rem auto;

        .col-4 {
            border: 1px solid $gh_gray;
            padding: 0.5rem;

            a {
                color: $gh_gray;

                &.active {
                    color: $gh_warning;
                }
            }
        }
    }
}
</style> 