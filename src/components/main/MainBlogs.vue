<script>
export default {
    name: 'MainBlogs',
    data() {
        return {
            message: '<svg xmlns="http://www.w3.org/2000/svg" height="0.875em" viewBox="0 0 640 512"><!--! Font Awesome Free 6.4.2 by @fontawesome - https://fontawesome.com License - https://fontawesome.com/license (Commercial License) Copyright 2023 Fonticons, Inc. --><path d="M208 352c114.9 0 208-78.8 208-176S322.9 0 208 0S0 78.8 0 176c0 38.6 14.7 74.3 39.6 103.4c-3.5 9.4-8.7 17.7-14.2 24.7c-4.8 6.2-9.7 11-13.3 14.3c-1.8 1.6-3.3 2.9-4.3 3.7c-.5 .4-.9 .7-1.1 .8l-.2 .2 0 0 0 0C1 327.2-1.4 334.4 .8 340.9S9.1 352 16 352c21.8 0 43.8-5.6 62.1-12.5c9.2-3.5 17.8-7.4 25.3-11.4C134.1 343.3 169.8 352 208 352zM448 176c0 112.3-99.1 196.9-216.5 207C255.8 457.4 336.4 512 432 512c38.2 0 73.9-8.7 104.7-23.9c7.5 4 16 7.9 25.2 11.4c18.3 6.9 40.3 12.5 62.1 12.5c6.9 0 13.1-4.5 15.2-11.1c2.1-6.6-.2-13.8-5.8-17.9l0 0 0 0-.2-.2c-.2-.2-.6-.4-1.1-.8c-1-.8-2.5-2-4.3-3.7c-3.6-3.3-8.5-8.1-13.3-14.3c-5.5-7-10.7-15.4-14.2-24.7c24.9-29 39.6-64.7 39.6-103.4c0-92.8-84.9-168.9-192.6-175.5c.4 5.1 .6 10.3 .6 15.5z"/></svg>',
            calendar: '<svg xmlns="http://www.w3.org/2000/svg" height="0.875em" viewBox="0 0 448 512"><!--! Font Awesome Free 6.4.2 by @fontawesome - https://fontawesome.com License - https://fontawesome.com/license (Commercial License) Copyright 2023 Fonticons, Inc. --><path d="M152 24c0-13.3-10.7-24-24-24s-24 10.7-24 24V64H64C28.7 64 0 92.7 0 128v16 48V448c0 35.3 28.7 64 64 64H384c35.3 0 64-28.7 64-64V192 144 128c0-35.3-28.7-64-64-64H344V24c0-13.3-10.7-24-24-24s-24 10.7-24 24V64H152V24zM48 192h80v56H48V192zm0 104h80v64H48V296zm128 0h96v64H176V296zm144 0h80v64H320V296zm80-48H320V192h80v56zm0 160v40c0 8.8-7.2 16-16 16H320V408h80zm-128 0v56H176V408h96zm-144 0v56H64c-8.8 0-16-7.2-16-16V408h80zM272 248H176V192h96v56z"/></svg>'
        }
    },
    props: [
        'title'
    ]

}
</script>

<template>
    <div class="d-flex flex-column align-items-center wrapper">
        <h1 class="text-capitalize text-center mt-5">{{ title }}</h1>
        <div class="splitter"></div>

        <div class="row">

            <div class="col-4">
                <img class="img-fluid" src="../../assets/img/Nisi-ut-aliquid-ex-ea-com.jpg" alt="">
                <div class="d-flex info align-items-center">
                    <div class="svg" v-html="calendar"></div>
                    <p>Jan 18,2021</p>
                    <div class="svg" v-html="message"></div>
                    <p>0 Comment</p>
                </div>
                <p>Anyway REPS is a NYC agency repres enting photographers</p>
            </div>

            <div class="col-4">
                <img class="img-fluid" src="../../assets/img/Architecto-beatae-vitae-dicta.jpg" alt="">
                <div class="d-flex info align-items-center">
                    <div class="svg" v-html="calendar"></div>
                    <p>May 30,2021</p>
                    <div class="svg" v-html="message"></div>
                    <p>0 Comment</p>
                </div>
                <p>Nasueal risuscipit Lorem Ipsum is simply text</p>
            </div>

            <div class="col-4">
                <img class="img-fluid" src="../../assets/img/At-vero-eos-et-accusamus.jpg" alt="">
                <div class="d-flex info align-items-center">
                    <div class="svg" v-html="calendar"></div>
                    <p>Apr 13,2021</p>
                    <div class="svg" v-html="message"></div>
                    <p>0 Comment</p>
                </div>
                <p>Nostrum Iesum Christum Lorem Ipsum is simply text</p>
            </div>
        </div>
    </div>
    <hr>
</template>


<style lang="scss" scoped>
@use '../../assets/scss/partials/splitter' as *;
@use '../../assets/scss/partials/variables' as *;

.svg {
    fill: $gh_warning;
    margin: 0;
    margin-right: 0.25rem;

}

.wrapper {
    margin-bottom: 4rem;

    .splitter {
        margin-top: 1rem;
        margin-bottom: 2rem;

    }

    .row {
        .col-4 {
            .info {
                p {
                    font-size: 13px;
                    color: $gh_gray;
                    margin: 0;
                    margin-right: 0.5rem;
                }
            }

            p {
                font-size: 15px;
            }
        }
    }
}
</style>