<script>
/* 
    
    fonte: https://github.com/luvejo/vue-3-carousel-tutorial 
    penso sia doveroso citare la fonte

*/
import SingleCard from './SingleCard.vue'
export default {
    name: 'MainCarousel',
    components: {
        SingleCard,

    },

    props: [
        'propStep'
    ],

    data() {
        return {
            star: '<svg xmlns="http://www.w3.org/2000/svg" height="1.25em" viewBox="0 0 576 512"><!--! Font Awesome Free 6.4.2 by @fontawesome - https://fontawesome.com License - https://fontawesome.com/license (Commercial License) Copyright 2023 Fonticons, Inc. --><path d="M316.9 18C311.6 7 300.4 0 288.1 0s-23.4 7-28.8 18L195 150.3 51.4 171.5c-12 1.8-22 10.2-25.7 21.7s-.7 24.2 7.9 32.7L137.8 329 113.2 474.7c-2 12 3 24.2 12.9 31.3s23 8 33.8 2.3l128.3-68.5 128.3 68.5c10.8 5.7 23.9 4.9 33.8-2.3s14.9-19.3 12.9-31.3L438.5 329 542.7 225.9c8.6-8.5 11.7-21.2 7.9-32.7s-13.7-19.9-25.7-21.7L381.2 150.3 316.9 18z"/></svg>',

            cards: [
                {
                    star: 4,
                    title: 'Shopping Mhajong connect',
                    image: 'src/assets/img/01-300x300.jpg',
                    discount: '$180.00',
                    price: '$100.00',
                    badge: '- 44%'
                },
                {
                    star: 0,
                    title: 'Buddy and Lucky Solitare',
                    image: 'src/assets/img/02-300x300.jpg',
                    price: '$83.00',
                    pricetwo: ' - $90.00',
                },
                {
                    star: 0,
                    title: 'Taishou x Alice Epilogue',
                    image: 'src/assets/img/03-300x300.jpg',
                    price: '$160.00',
                },
                {
                    star: 2,
                    title: 'Labyrinths of the World',
                    image: 'src/assets/img/04-300x300.jpg',
                    price: '$110.00',
                },
                {
                    star: 4,
                    title: 'Shopping Mhajong connect',
                    image: 'src/assets/img/05-300x300.jpg',
                    discount: '$180.00',
                    price: '$100.00',
                    badge: '- 44%'

                },
                {
                    star: 0,
                    title: 'Buddy and Lucky Solitare',
                    image: 'src/assets/img/06-300x300.jpg',
                    price: '$83.00',
                    pricetwo: ' - $90.00',
                },
                {
                    star: 0,
                    title: 'Taishou x Alice Epilogue',
                    image: 'src/assets/img/07-300x300.jpg',
                    price: '$160.00',
                },
                {
                    star: 2,
                    title: 'Labyrinths of the World',
                    image: 'src/assets/img/08-300x300.jpg',
                    price: '$110.00',
                },
                {
                    star: 4,
                    title: 'Shopping Mhajong connect',
                    image: 'src/assets/img/09-300x300.jpg',
                    discount: '$180.00',
                    price: '$100.00',
                    badge: '- 44%'
                },
                {
                    star: 0,
                    title: 'Buddy and Lucky Solitare',
                    image: 'src/assets/img/10-300x300.jpg',
                    price: '$83.00',
                    pricetwo: ' - $90.00',
                },
                {
                    star: 0,
                    title: 'Taishou x Alice Epilogue',
                    image: 'src/assets/img/11-300x300.jpg',
                    price: '$160.00',
                },
                {
                    star: 2,
                    title: 'Labyrinths of the World',
                    image: 'src/assets/img/12-300x300.jpg',
                    price: '$110.00',
                },
                {
                    star: 4,
                    title: 'Shopping Mhajong connect',
                    image: 'src/assets/img/13-300x300.jpg',
                    discount: '$180.00',
                    price: '$100.00',
                    badge: '- 44%'

                },
                {
                    star: 0,
                    title: 'Buddy and Lucky Solitare',
                    image: 'src/assets/img/14-300x300.jpg',
                    price: '$83.00',
                    pricetwo: ' - $90.00',
                },
                {
                    star: 0,
                    title: 'Taishou x Alice Epilogue',
                    image: 'src/assets/img/15-300x300.jpg',
                    price: '$160.00',
                },
                {
                    star: 2,
                    title: 'Labyrinths of the World',
                    image: 'src/assets/img/16-300x300.jpg',
                    price: '$110.00',
                },
                {
                    star: 0,
                    title: 'Taishou x Alice Epilogue',
                    image: 'src/assets/img/17-300x300.jpg',
                    price: '$160.00',
                },
                {
                    star: 2,
                    title: 'Labyrinths of the World',
                    image: 'src/assets/img/18-300x300.jpg',
                    price: '$110.00',
                },
            ],
            innerStyles: {},
            step: this.propStep,
            transitioning: false
        }
    },


    mounted() {
        this.resetTranslate()
        this.setStep()
    },

    methods: {
        setStep() {
            /* 
            calcola la larghezza interna totale 
            e calcola il valore necessario per andare avanti di una card  
            */
            const innerWidth = this.$refs.inner.scrollWidth
            const totalCards = this.cards.length
            this.step = `${innerWidth / totalCards}px`
        },

        next() {
            if (this.transitioning) return

            this.transitioning = true

            this.moveLeft()
            /* rimuove la prima card e la pusha alla fine  */
            this.afterTransition(() => {
                const card = this.cards.shift()
                this.cards.push(card)
                this.resetTranslate()
                this.transitioning = false
                this.setStep()
            })
        },

        prev() {
            if (this.transitioning) return

            this.transitioning = true

            this.moveRight()
            /* rimuove la card dalla fine e lo piazza all'inizio */
            this.afterTransition(() => {
                const card = this.cards.pop()
                this.cards.unshift(card)
                this.resetTranslate()
                this.transitioning = false
                this.setStep()

            })
        },

        /* moveLeft moveRight gestiscono la transizione per spostarsi */
        moveLeft() {
            this.innerStyles = {
                transform: `translateX(-${this.step})
                    translateX(-${this.step})`
            }
        },

        moveRight() {
            this.innerStyles = {
                transform: `translateX(${this.step})
                        translateX(-${this.step})`
            }
        },

        afterTransition(callback) {
            const listener = () => {
                callback()
                this.$refs.inner.removeEventListener('transitionend', listener)
            }
            this.$refs.inner.addEventListener('transitionend', listener)
        },

        resetTranslate() {
            this.innerStyles = {
                transition: 'none',
                transform: `translateX(-${this.step})`

            }
        }
    }
}
</script>

<template>
    <div class="carousel col-12 position-relative my-5   p-3">

        <div class="row align-items-center" ref="inner" :style="innerStyles">
            <SingleCard v-for="card in cards" :img="card.image" :title="card.title" :price="card.price"
                :pricetwo="card.pricetwo" :discount="card.discount" :stars="card.star" :badge="card.badge" />
        </div>
        <div class="command position-relative">
            <div class="position-absolute prev" @click="prev"></div>
            <div class="position-absolute next" @click="next"></div>
        </div>

    </div>
</template>


<style lang="scss" scoped>
.wrappper {
    width: 100%;
}

.carousel {
    overflow: hidden;

    .row {
        transition: transform 0.2s;
        flex-wrap: nowrap !important;
        transform: translateX(0px);
    }

    .command {
        .prev {
            height: 30px;
            width: 30px;
            background-image: url(../../../assets/img/arrow.png);
            background-position: 0px 30px;

            top: -280px;
            left: -15px;

            &:hover {
                background-position: 0px 0px;
            }

        }

        .next {
            height: 30px;
            width: 30px;
            background-image: url(../../../assets/img/arrow.png);
            background-position: 30px 30px;
            top: -280px;
            right: -16px;

            &:hover {
                background-position: 30px 0px;

            }

        }
    }
}
</style>