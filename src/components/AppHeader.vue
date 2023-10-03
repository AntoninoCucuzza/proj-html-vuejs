<script>
export default {
    name: 'AppHeader',
    data() {
        return {
            menu: [
                {
                    text: 'Home',
                    link: '#',
                },
                {
                    text: 'Shop',
                    link: '#',
                },
                {
                    text: 'Blog',
                    link: '#',
                },
                {
                    text: 'Media',
                    link: '#',
                },
                {
                    text: 'ShortCode',
                    link: '#',
                },
                {
                    text: 'Features',
                    link: '#',
                },
            ]
        }
    }
}
</script>
<template>
    <header id="app_header">
        <div class="d-flex flex-column">
            <div class="top d-flex justify-content-between align-items-center container">
                <div>
                    <a href="#" class="wish">Wishlist(0)</a>
                    <a href="#" class="help">Need help? </a>
                </div>
                <div>Call 24/7.800-8754-987</div>
            </div>
            <hr>
            <div class="bot container d-flex justify-content-between align-items-center">

                <div class="logo-img">
                    <a href="#"><img class="img-fluid" src="../assets/img/logo.png" alt=""></a>
                </div>

                <div class="menu">
                    <ul class="list-unstyled d-flex gap-5 m-0">
                        <li v-for="voice in menu"><a href="voice.link">{{ voice.text }}</a></li>
                    </ul>
                </div>

                <div class="d-flex align-items-center gap-4 utility">

                    <div class="serchbar">
                        <svg xmlns="http://www.w3.org/2000/svg" height="1.25em"
                            viewBox="0 0 512 512"><!--! Font Awesome Free 6.4.2 by @fontawesome - https://fontawesome.com License - https://fontawesome.com/license (Commercial License) Copyright 2023 Fonticons, Inc. -->
                            <path
                                d="M416 208c0 45.9-14.9 88.3-40 122.7L502.6 457.4c12.5 12.5 12.5 32.8 0 45.3s-32.8 12.5-45.3 0L330.7 376c-34.4 25.2-76.8 40-122.7 40C93.1 416 0 322.9 0 208S93.1 0 208 0S416 93.1 416 208zM208 352a144 144 0 1 0 0-288 144 144 0 1 0 0 288z" />
                        </svg>
                    </div>
                    <div class="user">
                        <svg xmlns="http://www.w3.org/2000/svg" height="1.25em"
                            viewBox="0 0 448 512"><!--! Font Awesome Free 6.4.2 by @fontawesome - https://fontawesome.com License - https://fontawesome.com/license (Commercial License) Copyright 2023 Fonticons, Inc. -->
                            <path
                                d="M304 128a80 80 0 1 0 -160 0 80 80 0 1 0 160 0zM96 128a128 128 0 1 1 256 0A128 128 0 1 1 96 128zM49.3 464H398.7c-8.9-63.3-63.3-112-129-112H178.3c-65.7 0-120.1 48.7-129 112zM0 482.3C0 383.8 79.8 304 178.3 304h91.4C368.2 304 448 383.8 448 482.3c0 16.4-13.3 29.7-29.7 29.7H29.7C13.3 512 0 498.7 0 482.3z" />
                        </svg>
                    </div>
                    <div class="carrello ">
                        <svg xmlns="http://www.w3.org/2000/svg" height="1.25em"
                            viewBox="0 0 448 512"><!--! Font Awesome Free 6.4.2 by @fontawesome - https://fontawesome.com License - https://fontawesome.com/license (Commercial License) Copyright 2023 Fonticons, Inc. -->
                            <path
                                d="M160 112c0-35.3 28.7-64 64-64s64 28.7 64 64v48H160V112zm-48 48H48c-26.5 0-48 21.5-48 48V416c0 53 43 96 96 96H352c53 0 96-43 96-96V208c0-26.5-21.5-48-48-48H336V112C336 50.1 285.9 0 224 0S112 50.1 112 112v48zm24 48a24 24 0 1 1 0 48 24 24 0 1 1 0-48zm152 24a24 24 0 1 1 48 0 24 24 0 1 1 -48 0z" />
                        </svg>
                        <span>(0) $0.00</span>
                    </div>
                </div>

            </div>
        </div>
    </header>
</template>


<style lang="scss" scoped>
@use '../assets/scss/partials/variables' as *;

header {
    background-color: $gh_dark_violet ;

    .top {
        padding: 0.25rem;
        color: gray;

        a {
            color: gray;
        }

        .wish {
            padding-right: 0.5rem;
            border-right: 2px solid gray;
        }

        .help {
            padding-left: 0.5rem;

        }
    }

    hr {
        margin: 0;
    }

    .bot {
        padding: 1rem;

        .menu {
            a {
                transition: all 0.2s;

                &:hover {
                    color: $gh_warning;
                }

            }
        }

        .utility {
            fill: #fff;

            .carrello {
                svg {
                    margin-right: 0.5rem;
                }

                span {
                    color: $gh_warning ;
                }
            }
        }
    }
}
</style>