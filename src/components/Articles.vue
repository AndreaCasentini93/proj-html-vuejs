<template>
    <section class="position-relative">
        <!-- DECORATIONS -->
        <svg xmlns="http://www.w3.org/2000/svg" width="200" height="202" fill="#B2E0F6" class="cloud">
            <path class="elementor-shape-fill" d="M139.374 198.088c16.328 8.906 51.35-1.087 58.304-39.038 7.15-39.022-13.182-40.052-9.633-54.248 14.243-21.15 16.782-48.14 2.028-64.387-36.503-38.024-45.629 7.604-76.048-20.28C101.727 7.837 83.1-6.735 56.23 3.405 18.239 17.74 27.33 47.659 27.33 69.313c0 7.624-24.216 21.957-26.87 41.573-3.346 24.734 12.168 57.29 26.87 68.443 23.322 26.363 59.318 20.28 75.541 11.154 13.931-7.836 25.35 1.52 36.503 7.605z"/>
        </svg>
        <img class="string" src="../assets/images/maxcoach-shape-14.png" alt="string">
        <img class="dotted_circle" src="../assets/images/maxcoach-shape-05.png" alt="dotted_circle">
        <div class="ring"></div>
        <!-- /DECORATIONS -->

        <div class="container">
            <!-- TITLE -->
            <div>Title</div>
            <!-- /TITLE -->

            <!-- CARDS -->
            <div>Cards</div>
            <!-- /CARDS -->

            <!-- GET INTO -->
            <div class="text-center">
                <div class="get_into">Get into details now? <a href="#">View all posts &#x2192;</a></div>
            </div>
            <!-- /GET INTO -->
        </div>
    </section>
</template>

<script>
export default {
    name: 'Articles'
}
</script>

<style lang="scss" scoped>
    @import '../assets/style/variables.scss';
    @import '../assets/style/mixins.scss';

    section {
        height: 600px;
        background-color: $bg-articles;
        overflow: hidden;
        z-index: -1;

        & > img {
            position: absolute;
            z-index: -1;
        }

        .cloud {
            position: absolute;
            top: 0;
            right: 0;
            transform: scale(.8);
            z-index: -1;
        }

        .string {
            top: 35%;
            left: 0;
            width: 100%;
            filter: contrast(20%) sepia(100%);
        }

        .dotted_circle {
            top: 0;
            left: 0;
            width: 120px
        }

        .ring {
            @include ring;
            top: 0;
            left: 0;
            z-index: -1;
        }

        .container {
            z-index: 1;

            .get_into {
                font-size: 13px;
                color: $base-color;

                a {
                    font-size: 13px;
                    color: $ashtag-color;
                }
            }
        }
    }
</style>