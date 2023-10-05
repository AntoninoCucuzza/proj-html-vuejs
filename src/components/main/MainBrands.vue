
<script>
export default {
    name: 'MainBrands',
    data() {
        return {

            brands: [
                {
                    name: 'White Wols',
                    logo: '../../assets/img/brand-01.png',
                    link: '#',
                },

                {
                    name: 'Fighters1',
                    logo: '../../assets/img/brand-02.png',
                    link: '#',
                },

                {
                    name: 'Tigers',
                    logo: '../../assets/img/brand-03.png',
                    link: '#',
                },

                {
                    name: 'Rhino',
                    logo: '../../assets/img/brand-04.png',
                    link: '#',
                },

                {
                    name: 'B2Jersey',
                    logo: '../../assets/img/brand-05.png',
                    link: '#',
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
    <div class="row my-5">
        <div class="col" v-for="brand in brands">
            <a href="brand.link">
                <img :src="getImg(brand.logo)" :alt="brand.name">
            </a>
        </div>
    </div>
</template>

<style lang="scss" scoped></style>