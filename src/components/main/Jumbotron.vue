<script>
export default {
    name: 'Jumbotron'
}
</script>
<template>
    <div class="jumbo d-flex flex-column align-items-center justify-content-center">
        <div class="container p-3">
            <h2 class="warning">Upcoming Stock</h2>
            <h1 class="title my-4"><span>R</span>esident <span>E</span>vil 3 <br><span>Remake</span></h1>
            <div class="btn btn-light mt-5">Shop Now</div>
        </div>
    </div>
</template>

<style lang="scss" scoped>
@use '../../assets/scss/partials/variables' as *;

.jumbo {
    height: 750px;
    background-image: url(https://image.api.playstation.com/vulcan/ap/rnd/202206/0307/wIVJREWyBg8SyXvXYuBPG6je.png);
    background-repeat: no-repeat;
    background-size: cover;

    .container {
        .warning {
            font-weight: 700;
            display: inline-block;
            padding: 0.25rem 2rem;
            color: $gh_black;
            background-color: $gh_warning;
            clip-path: polygon(10% 0, 100% 0, 90% 100%, 0 100%);
        }

        .title {
            font-size: 3.5rem;

            span {
                color: $gh_danger;
            }
        }

        .btn {
            border-radius: 0;
            font-weight: 700;

            &:hover {
                background-color: $gh_warning ;
                border-color: $gh_black;

            }
        }
    }
}
</style>