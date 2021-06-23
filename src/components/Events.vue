<template>
    <section class="position-relative">
        <!-- DECORATIONS -->
        <svg xmlns="http://www.w3.org/2000/svg" width="200" height="202" fill="#FEF7F3" class="cloud">
            <path class="elementor-shape-fill" d="M139.374 198.088c16.328 8.906 51.35-1.087 58.304-39.038 7.15-39.022-13.182-40.052-9.633-54.248 14.243-21.15 16.782-48.14 2.028-64.387-36.503-38.024-45.629 7.604-76.048-20.28C101.727 7.837 83.1-6.735 56.23 3.405 18.239 17.74 27.33 47.659 27.33 69.313c0 7.624-24.216 21.957-26.87 41.573-3.346 24.734 12.168 57.29 26.87 68.443 23.322 26.363 59.318 20.28 75.541 11.154 13.931-7.836 25.35 1.52 36.503 7.605z"/>
        </svg>
        <img class="jagged_circle" src="../assets/images/maxcoach-shape-13.png" alt="jagged_circle">
        <img class="form_2 hidden_991px" src="../assets/images/artist-shape-02.png" alt="form_2">
        <div class="text_decoration hidden_991px">Events</div>
        <!-- /DECORATIONS -->

        <!-- CONTAINER -->
        <div class="container">
            <div class="row">
                <div class="col-10 offset-1">
                    <!-- TITLE -->
                    <div class="text-center title">
                        <h2>Upcoming Events</h2>
                        <h3>Let's Work Together</h3>
                    </div>
                    <!-- /TITLE -->

                    <!-- CARDS -->
                    <div class="row events_cards">
                        <Card v-for="singleCard,index in cards" :key="index" class="col-12 col-md-6" :card="singleCard"/>
                    </div>
                    <!-- /CARDS -->
                </div>
            </div>
        </div>
        <!-- /CONTAINER -->
    </section>
</template>

<script>
import Card from './Card.vue';

export default {
    name: 'Events',
    components: {
        Card
    },
    data: function() {
        return {
            cards: [
                {
                    title: 'Storytelling Workshop',
                    image: require('../assets/images/artist-event-04-250x300.jpg'),
                    subTitle: 'NOV 22, 2020',
                    classIcon1: 'fas fa-map-marker-alt',
                    classIcon2: '',
                    textIcon1: 'Texas, US',
                    textIcon2: ''
                },
                {
                    title: 'Painting Art Contest 2020',
                    image: require('../assets/images/artist-event-03-250x300.jpg'),
                    subTitle: 'OCT 10, 2020',
                    classIcon1: 'fas fa-map-marker-alt',
                    classIcon2: '',
                    textIcon1: 'New York, US',
                    textIcon2: ''
                },
                {
                    title: 'International Art Fair 2020',
                    image: require('../assets/images/artist-event-02-250x300.jpg'),
                    subTitle: 'NOV 23, 2020',
                    classIcon1: 'fas fa-map-marker-alt',
                    classIcon2: '',
                    textIcon1: 'Hamburg, Germany',
                    textIcon2: ''
                },
                {
                    title: 'Street Performance: Call for Artist',
                    image: require('../assets/images/artist-event-01-250x300.jpg'),
                    subTitle: 'DEC 15, 2020',
                    classIcon1: 'fas fa-map-marker-alt',
                    classIcon2: '',
                    textIcon1: 'Illinois, US',
                    textIcon2: ''
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
        padding: 60px 20px;
        overflow: hidden;

        & > img {
            position: absolute;
        }

        .cloud {
            position: absolute;
            top: 20%;
            right: 0%;
            transform: scale(1.3);
        }

        .form_2 {
            bottom: 0;
            left: -9%;
            width: 400px;
            transform: rotate(270deg);
        }

        .jagged_circle {
            top: 13%;
            right: 0;
            width: 140px;
        }

        .text_decoration {
            position: absolute;
            top: 45%;
            left: -6%;
            font-size: 120px;
            font-family: $decoration-font;
            color: lighten($ashtag-color, 35%);
            transform: rotate(90deg);
            z-index: -1;
        }

        .container {

            .title {
                h2 {
                    @include section-title-35px;
                }

                h3 {
                    line-height: 1;
                    margin-bottom: 50px;
                    font-size: 25px;
                    font-weight: 700;
                    color: $sub-title-color;
                }
            }

        }
    }

    @media screen and (max-width: 991px) {
        
        .hidden_991px {
            display: none !important;
        }

        h2 {
            font-size: 30px !important;
        }

        h3 {
            font-size: 20px !important;
        }

        h4 {
            font-size: 13px !important;
        }

        h5 {
            font-size: 12px !important;
        }

        p {
            font-size: 11px !important;
        }
    }

</style>