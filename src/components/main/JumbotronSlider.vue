<script>
export default {
    name: 'JumbotronSlider',
    data() {
        return {
            activeSlide: 0,
            slides: [
                {
                    image: "src/assets/img/t5-1-100x100_left.jpg",
                    name: "Luies Charls",
                    role: "Web Designer",
                    description: "Lorem ipsum dolor, sit amet consectetur adipisicing elit. Veniam quos magni, sunt laudantium aut, maiores veritatis omnis soluta iusto quidem est assumenda laborum provident, cumque obcaecati libero? Commodi, nihil ipsum. Lorem ipsum dolor sit amet consectetur adipisicing elit."
                },
                {
                    image: "src/assets/img/t4-1-100x100_left.jpg",
                    name: "Mario bros",
                    role: "Idraulico",
                    description: " oltre a fare l'idraulico salva la stessa principessa dal 1985 dalla stessa indentica tartaruga sotto steroidi a cui hanno appiccicato delle spine sul guscio"
                },
                {
                    image: "src/assets/img/t2-1-100x100_left.jpg",
                    name: "Luigi bros",
                    role: "Idraulico",
                    description: "fratello di Mario anche lui un idraulico ma ogni tra un rewatch di Ghostbuster e uno dell'esorciccio si diverte a far cosplay in ville abbandonate e si immagina di assorbire fantasmi con una aspirapolvere, sotto effetto di qualcosa? poesse"
                }
            ]
        }
    },
    methods: {
        changeSlide(i) {
            this.activeSlide = i
            console.log(this.activeSlide);
        }
    }
}
</script>

<template>
    <div class="bg">
        <div class="container h-100 ">
            <div class="row h-100 justify-content-center align-items-center ">
                <div class="col-12 d-flex align-items-center flex-column ">

                    <div v-for="(slide, i) in slides" class="card-wrapper">
                        <div v-if="i === activeSlide" class=" d-flex align-items-center flex-column">

                            <div class="img-wrapper position-relative">

                                <img class="img-fluid plot" :src="slide.image" alt="">
                                <div class="position-absolute quote"></div>

                            </div>

                            <div class="about py-4">
                                <h4>{{ slide.name }} <span>({{ slide.role }})</span></h4>
                            </div>

                            <div class="description my-3">
                                {{ slide.description }}
                            </div>
                        </div>

                    </div>


                    <div class="d-flex tools ">
                        <div v-for="(ball, i) in 3" @click="changeSlide(i)" class="balls"
                            :class="i === activeSlide ? 'active' : ''"></div>

                    </div>
                </div>

            </div>
        </div>
    </div>
</template>

<style lang="scss" scoped>
@use '../../assets/scss/partials/variables' as *;

.bg {
    height: 600px;
    background-image: url(../../assets/img/parallax.jpg);
    background-repeat: no-repeat;
    background-size: cover;
    background-position: bottom;

    .col-12 {
        .img-wrapper {
            .plot {
                border: 3px solid $gh_warning;
                border-radius: 50%;
            }

            .quote {
                top: 0;
                left: 0;
                height: 30px;
                width: 30px;
                padding: 0.25rem;
                border-radius: 50%;
                background-color: $gh_warning ;
                background-image: url(../../assets/img/quote.png);
                background-repeat: no-repeat;
                background-position: center;
            }
        }

        .about {
            span {
                color: $gh_warning;
            }
        }

        .description {
            color: $gh_gray;
            text-align: center;
        }

        .tools {
            margin-top: 4rem;

            .balls {
                background-color: $gh_white;
                border-radius: 50%;
                height: 15px;
                width: 15px;
                margin: 0.5rem;
                transition: all 0.2s;
            }

            .active {
                background-color: $gh_warning !important;
                scale: 1.3;
                filter: drop-shadow(0px 0px 5px $gh_warning);
            }


        }
    }
}
</style>