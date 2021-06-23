<template>
    <section class="position-relative">
        <!-- DECORATIONS -->
        <svg xmlns="http://www.w3.org/2000/svg" width="200" height="202" fill="#B2E0F6" class="cloud hidden_991px">
            <path class="elementor-shape-fill" d="M139.374 198.088c16.328 8.906 51.35-1.087 58.304-39.038 7.15-39.022-13.182-40.052-9.633-54.248 14.243-21.15 16.782-48.14 2.028-64.387-36.503-38.024-45.629 7.604-76.048-20.28C101.727 7.837 83.1-6.735 56.23 3.405 18.239 17.74 27.33 47.659 27.33 69.313c0 7.624-24.216 21.957-26.87 41.573-3.346 24.734 12.168 57.29 26.87 68.443 23.322 26.363 59.318 20.28 75.541 11.154 13.931-7.836 25.35 1.52 36.503 7.605z"/>
        </svg>
        <img class="string" src="../assets/images/maxcoach-shape-14.png" alt="string">
        <img class="dotted_circle hidden_991px" src="../assets/images/maxcoach-shape-05.png" alt="dotted_circle">
        <div class="ring hidden_991px"></div>
        <!-- /DECORATIONS -->

        <div class="container">
            <!-- TITLE -->
            <div class="text-center">
                <h2>Articles and Tips</h2>
                <h3>Latest from the blog</h3>
            </div>
            <!-- /TITLE -->

            <!-- CARDS -->
            <div class="d-flex justify-content-center flex-wrap articles_cards">
                <Card v-for="singleCard,index in cards" :key="index" :card="singleCard"/>
            </div>
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
import Card from './Card.vue';

export default {
    name: 'Articles',
    components: {
        Card
    },
    data: function() {
        return {
            cards: [
                {
                    title: 'Brush Strokes Energize Trees in Paintings',
                    image: require('../assets/images/artist-blog-03-480x356.jpeg'),
                    subTitle: 'Artist',
                    classIcon1: 'far fa-calendar',
                    classIcon2: 'far fa-eye',
                    textIcon1: 'May 15, 2020',
                    textIcon2: '688 views'
                },
                {
                    title: 'Connection Between Self-Portraits and Identity',
                    image: require('../assets/images/artist-blog-02-500x680.jpg'),
                    subTitle: 'Artist',
                    classIcon1: 'far fa-calendar',
                    classIcon2: 'far fa-eye',
                    textIcon1: 'May 15, 2020',
                    textIcon2: '397 views'
                },
                {
                    title: 'Pocket-Sized Notebooks Hold Miniature Paintings',
                    image: require('../assets/images/artist-blog-01-480x356.jpg'),
                    subTitle: 'Artist',
                    classIcon1: 'far fa-calendar',
                    classIcon2: 'far fa-eye',
                    textIcon1: 'May 15, 2020',
                    textIcon2: '603 views'
                }
            ]
        }
    }
}
</script>

<style lang="scss" scoped>
    @import '../assets/style/variables.scss';
    @import '../assets/style/mixins.scss';

    section {
        padding: 60px 0;
        background-color: $bg-articles;
        overflow: hidden;

        & > img {
            position: absolute;
        }

        .cloud {
            position: absolute;
            bottom: 7%;
            right: 30%;
            transform: scale(.8);
        }

        .string {
            top: 30%;
            left: 0;
            width: 100%;
            filter: contrast(20%) sepia(100%);
        }

        .dotted_circle {
            top: 17%;
            left: 32%;
            width: 120px
        }

        .ring {
            @include ring;
            top: 20%;
            left: 15%;
        }

        .container {
            z-index: 1;

            div {
                h2 {
                    @include section-title-35px;
                }

                h3 {
                    line-height: 1.5;
                    margin-bottom: 50px;
                    font-size: 25px;
                    font-weight: 700;
                    color: $sub-title-color;
                }
            }

            .get_into {
                margin-top: 65px;
                font-size: 13px;
                color: $base-color;

                a {
                    border-bottom: 2px solid #EEF0F1;
                    font-size: 13px;
                    font-weight: 700;
                    color: $ashtag-color;
                    @include transition-type-1(color);

                    &:hover {
                        color: lighten($ashtag-color, 20%);
                    }
                }
            }
        }
    }

    @media screen and (max-width: 991px) {
        .hidden_991px {
            display: none;
        }
    }
</style>