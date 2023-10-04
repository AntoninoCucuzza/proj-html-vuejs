<script>
import Jumbotron from './main/Jumbotron.vue';
import MainService from './main/MainService.vue'
import AppGames from './main/AppGames.vue';
import SpecialCategory from './main/SpecialCategory.vue';
import MainDeals from './main/MainDeals.vue';
import JumbotronSlider from './main/JumbotronSlider.vue';
import MainBlogs from './main/MainBlogs.vue';
import AppFooter from './AppFooter.vue'

export default {
    name: 'AppMain',
    data() {
        return {
            popular: 'src/assets/img/cms-banner-01.jpg',
            latest: 'src/assets/img/cms-banner-02.jpg',
            discount: 'src/assets/img/cms-banner-03.jpg',
            medDiscount: 'src/assets/img/cms-banner-04.jpg',
            brands: [
                {
                    name: 'White Wols',
                    logo: 'src/assets/img/brand-01.png',
                    link: '#',
                },

                {
                    name: 'Fighters1',
                    logo: 'src/assets/img/brand-02.png',
                    link: '#',
                },

                {
                    name: 'Tigers',
                    logo: 'src/assets/img/brand-03.png',
                    link: '#',
                },

                {
                    name: 'Rhino',
                    logo: 'src/assets/img/brand-04.png',
                    link: '#',
                },

                {
                    name: 'B2Jersey',
                    logo: 'src/assets/img/brand-05.png',
                    link: '#',
                },
            ]

        }
    },
    components: {
        Jumbotron,
        AppGames,
        SpecialCategory,
        MainService,
        MainDeals,
        JumbotronSlider,
        MainBlogs,
        AppFooter
    }
}
</script>
<template>
    <Jumbotron />
    <div class="container">

        <MainService />

        <AppGames :firstImg="popular" :firstType="'Most Popular'" :firstName="'The Battlefield 4'"
            :firstInfo="'Naval Strike'" :secondImg="latest" :secondType="'Latest Game'" :secondName="`Assassin's Creed`"
            :secondInfo="'Unity Game'" />

        <SpecialCategory />

        <MainDeals :isTrue="false" :title="'our products'" />

        <AppGames :firstImg="discount" :firstType="'20% Discount'" :firstName="`Dragon's Dogma`" :firstInfo="'Video Game'"
            :secondImg="medDiscount" :secondType="'30% Discount'" :secondName="'World Of Tanks'" :secondInfo="'New Game'" />

        <MainDeals :isTrue="true" :title="'deal of the day'" />
    </div>
    <JumbotronSlider />

    <div class="container">
        <MainBlogs :title="'new game blogs'" />
        <div class="row my-5">
            <div class="col" v-for="brand in brands">
                <a href="brand.link">
                    <img :src="brand.logo" :alt="brand.name">
                </a>
            </div>
        </div>
    </div>
    <AppFooter />
</template>


<style lang="scss" scoped>
@use '../assets/scss/partials/variables' as *;
</style>