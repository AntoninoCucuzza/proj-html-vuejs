<script>
export default {
    name: 'AppGames',
    props: [
        'firstImg',
        'firstType',
        'firstName',
        'firstInfo',

        'secondImg',
        'secondType',
        'secondName',
        'secondInfo',


    ],
}
</script>

<template>
    <div class="row my-5">
        <div class="col-6 position-relative">
            <div class="position-absolute text_position">
                <h3 class="warning">{{ firstType }}</h3>
                <h2>{{ firstName }}</h2>
                <h2>{{ firstInfo }}</h2>

            </div>
            <img class="img-fluid" :src="firstImg" alt="">
        </div>

        <div class="col-6 position-relative">
            <div class="position-absolute text_position">
                <h3 class="warning">{{ secondType }}</h3>
                <h2>{{ secondName }}</h2>
                <h2>{{ secondInfo }}</h2>
            </div>
            <img class="img-fluid" :src="secondImg" alt="">
        </div>
    </div>
</template>


<style lang="scss" scoped>
@use '../../assets/scss/partials/variables' as *;

.row {
    .col-6 {
        .text_position {
            top: 45%;
            left: 60%;
            transform: translate(-45%, -50%);

            .warning {
                font-weight: 700;
                display: inline-block;
                padding: 0.25rem 2rem;
                color: $gh_black;
                background-color: $gh_warning;
                clip-path: polygon(10% 0, 100% 0, 90% 100%, 0 100%);
            }

        }
    }
}
</style>