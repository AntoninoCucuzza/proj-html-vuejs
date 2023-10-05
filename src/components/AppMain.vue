<script>
import Jumbotron from './main/Jumbotron.vue';
import MainService from './main/MainService.vue'
import AppGames from './main/AppGames.vue';
import SpecialCategory from './main/SpecialCategory.vue';
import MainDeals from './main/MainDeals.vue';
import JumbotronSlider from './main/JumbotronSlider.vue';
import MainBlogs from './main/MainBlogs.vue';
import MainCarousel from './main/carousel/MainCarousel.vue';
import MainBrands from './main/MainBrands.vue'

export default {
    name: 'AppMain',
    data() {
        return {
            popular: 'src/assets/img/cms-banner-01.jpg',
            latest: 'src/assets/img/cms-banner-02.jpg',
            discount: 'src/assets/img/cms-banner-03.jpg',
            medDiscount: 'src/assets/img/cms-banner-04.jpg',
        }
    },
    components: {
        Jumbotron,
        AppGames,
        SpecialCategory,
        MainService,
        MainDeals,
        JumbotronSlider,
        MainBrands,
        MainBlogs,
        MainCarousel
    },

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
        <!-- negazione della condizione -->
        <MainDeals :isTrue="false" :title="'our products'" />

        <MainCarousel :propStep="'0px'" />

        <AppGames :firstImg="discount" :firstType="'20% Discount'" :firstName="`Dragon's Dogma`" :firstInfo="'Video Game'"
            :secondImg="medDiscount" :secondType="'30% Discount'" :secondName="'World Of Tanks'" :secondInfo="'New Game'" />

        <!-- conferma della condizione -->
        <MainDeals :isTrue="true" :title="'deal of the day'" />

        <MainCarousel :propStep="'1296px'" />

    </div>
    <JumbotronSlider />

    <div class="container">
        <MainBlogs :title="'new game blogs'" />
        <MainBrands />
    </div>
</template>


<style lang="scss" scoped>
@use '../assets/scss/partials/variables' as *;
</style>