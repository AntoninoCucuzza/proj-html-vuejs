<script>
export default {
    name: 'AppHeader',
    data() {
        return {

        }
    }
}
</script>
<template>
    <header>
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
                <div>
                    <ul class="list-unstyled d-flex gap-5 m-0">
                        <li>Home</li>
                        <li>Shop</li>
                        <li>Blog</li>
                        <li>Media</li>
                        <li>ShortCode</li>
                        <li>Features</li>
                    </ul>
                </div>

                <div>

                    lente user carrello
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
    }
}
</style>