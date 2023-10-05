<script>
export default {
    data() {
        return {
            position: '<svg xmlns="http://www.w3.org/2000/svg" height="0.875em" viewBox="0 0 384 512"><!--! Font Awesome Free 6.4.2 by @fontawesome - https://fontawesome.com License - https://fontawesome.com/license (Commercial License) Copyright 2023 Fonticons, Inc. --><path d="M215.7 499.2C267 435 384 279.4 384 192C384 86 298 0 192 0S0 86 0 192c0 87.4 117 243 168.3 307.2c12.3 15.3 35.1 15.3 47.4 0zM192 128a64 64 0 1 1 0 128 64 64 0 1 1 0-128z"/></svg>',
            mail: '<svg xmlns="http://www.w3.org/2000/svg" height="0.875em" viewBox="0 0 512 512"><!--! Font Awesome Free 6.4.2 by @fontawesome - https://fontawesome.com License - https://fontawesome.com/license (Commercial License) Copyright 2023 Fonticons, Inc. --><path d="M48 64C21.5 64 0 85.5 0 112c0 15.1 7.1 29.3 19.2 38.4L236.8 313.6c11.4 8.5 27 8.5 38.4 0L492.8 150.4c12.1-9.1 19.2-23.3 19.2-38.4c0-26.5-21.5-48-48-48H48zM0 176V384c0 35.3 28.7 64 64 64H448c35.3 0 64-28.7 64-64V176L294.4 339.2c-22.8 17.1-54 17.1-76.8 0L0 176z"/></svg>',
            phone: '<svg xmlns="http://www.w3.org/2000/svg" height="0.875em" viewBox="0 0 512 512"><!--! Font Awesome Free 6.4.2 by @fontawesome - https://fontawesome.com License - https://fontawesome.com/license (Commercial License) Copyright 2023 Fonticons, Inc. --><path d="M164.9 24.6c-7.7-18.6-28-28.5-47.4-23.2l-88 24C12.1 30.2 0 46 0 64C0 311.4 200.6 512 448 512c18 0 33.8-12.1 38.6-29.5l24-88c5.3-19.4-4.6-39.7-23.2-47.4l-96-40c-16.3-6.8-35.2-2.1-46.3 11.6L304.7 368C234.3 334.7 177.3 277.7 144 207.3L193.3 167c13.7-11.2 18.4-30 11.6-46.3l-40-96z"/></svg>',
        }
    },

    props: [
        'infos',
        'extras',
        'socials',
    ]
}
</script>

<template>
    <footer class="wrapper">
        <div class="container area">
            <div class="row">
                <div class="col-3">
                    <h4 class="mb-4">Address Info</h4>

                    <div class="d-flex info">
                        <div class="svg" v-html="position"></div>
                        <p>60 29th Street San Francisco CA 94110 507-Union Trade Center, United States of America</p>
                    </div>

                    <div class="d-flex info">
                        <div class="svg" v-html="phone"></div>
                        <p>(+00) 123-456-789</p>

                    </div>

                    <div class="d-flex info">
                        <div class="svg" v-html="mail"></div>
                        <p>demo@example.com</p>

                    </div>
                </div>
                <div class="col-3">
                    <h4 class="mb-4">Information</h4>
                    <ul class="list-unstyled">
                        <li v-for="info in infos" class="py-1">
                            <a href="info.link">{{ info.title }}</a>
                        </li>
                    </ul>
                </div>
                <div class="col-3">
                    <h4 class="mb-4">Extras</h4>
                    <ul class="list-unstyled">
                        <li v-for="extra in extras" class="py-1">
                            <a href="extra.link">{{ extra.title }}</a>
                        </li>
                    </ul>
                </div>
                <div class="col-3">
                    <h4 class="mb-4">Our Newsletter</h4>
                    <div class="newsletter">
                        <p>There are many varations of passages of form humour or randomised </p>
                        <input type="text">
                        <div class="d-flex socials">
                            <a class="social" v-for="social in socials " :href="social.link" v-html="social.icon"></a>
                        </div>

                    </div>
                </div>
            </div>
        </div>
        <hr>
        <div class="container bot">
            <div class="d-flex justify-content-between">
                <div class="left">Copyright &copy; 2023 Codezeel</div>
                <div class="right">
                    <div class="wrapper d-flex">
                        <div class="single-img american"></div>
                        <div class="single-img discover"></div>
                        <div class="single-img mastercard"></div>
                        <div class="single-img paypal"></div>
                        <div class="single-img visa"></div>

                    </div>
                </div>
            </div>
        </div>
    </footer>
</template>


<style lang="scss" scoped>
@use '../assets/scss/partials/variables' as *;

footer {
    background-image: url(../assets/img/footer-bg.png);

    .area {
        padding: 6rem;

        .row {
            .col-3 {
                .info {
                    .svg {
                        fill: $gh_warning;
                        margin-right: 1rem;
                    }

                    p {
                        color: $gh_gray;
                    }
                }

                .newsletter {
                    p {
                        color: $gh_gray;

                    }

                    input {
                        padding: 0.5rem;
                        border: none;
                        width: 300px;
                        background-image: url(../assets/img/newsletter.png);
                        background-repeat: no-repeat;
                        background-position: 265px 10px;
                        transition: background-color 0.3s;

                        &:hover {
                            background-position: 265px -54px;
                            background-color: $gh_violet_darker;
                            box-shadow: $gh_dark_violet 0px 0px 20px 3px;
                        }
                    }

                    .socials {
                        .social {
                            padding: 0.5rem;
                            fill: $gh_white;

                            &:hover {
                                filter: drop-shadow(0px 0px 5px $gh_warning);
                                fill: $gh_warning;
                            }
                        }
                    }
                }

                ul {
                    a {
                        color: $gh_gray ;
                        transition: 0.2s;

                        &:hover {
                            color: $gh_warning;
                        }
                    }
                }
            }
        }
    }

    .left {
        color: $gh-gray;
    }

    .right {
        .single-img {
            width: 50px;
            height: 35px;
            background-image: url(../assets/img/payments.png);
            background-repeat: no-repeat;

        }

        .american {
            background-position: 0px -236px;
        }

        .discover {
            background-position: 0px -195px;
        }

        .mastercard {
            background-position: 0px -39px;
        }

        .paypal {
            background-position: 0px -116px;
        }

        .visa {
            background-position: 0px 0px;
        }
    }
}
</style>