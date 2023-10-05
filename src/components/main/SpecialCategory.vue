<script>
export default {
    name: 'SpecialCategory',
    data() {
        return {

            games: [
                {
                    name: 'Battlefield 3',
                    img: '../../assets/img/category-image-02-446x550_t.jpg',
                },
                {
                    name: 'Pubg',
                    img: '../../assets/img/category-image-01-446x550_t.jpg',
                },
                {
                    name: 'Jump Force',
                    img: '../../assets/img/category-image-03-446x550_t.jpg',
                },
            ]
        }
    },
    methods: {
        getImg(url) {
            return new URL(`${url}`, import.meta.url).href
        },
    }

}
</script>
<template>
    <div class="row my-5 flex-column align-items-center ">
        <h1 class=" text-center m-0">Special Category</h1>
        <div class="splitter my-3"></div>
        <div class="row">
            <div class="col-4" v-for="game in games">
                <div class="overlay-wrapper">
                    <div class="overlay position-absolute">
                        <h5> {{ game.name }}</h5>
                        <a href="#">Shop Now</a>
                    </div>
                    <img :title="game.name" class="img-fluid" :src="getImg(game.img)" alt="">
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