<template>
    <section class="position-relative">
        <!-- DECORATIONS -->
        <svg xmlns="http://www.w3.org/2000/svg" width="200" height="202" fill="#FEF7F3" class="cloud">
            <path class="elementor-shape-fill" d="M139.374 198.088c16.328 8.906 51.35-1.087 58.304-39.038 7.15-39.022-13.182-40.052-9.633-54.248 14.243-21.15 16.782-48.14 2.028-64.387-36.503-38.024-45.629 7.604-76.048-20.28C101.727 7.837 83.1-6.735 56.23 3.405 18.239 17.74 27.33 47.659 27.33 69.313c0 7.624-24.216 21.957-26.87 41.573-3.346 24.734 12.168 57.29 26.87 68.443 23.322 26.363 59.318 20.28 75.541 11.154 13.931-7.836 25.35 1.52 36.503 7.605z"/>
        </svg>
        <img class="jagged_circle" src="../assets/images/maxcoach-shape-13.png" alt="jagged_circle">
        <img class="form_2" src="../assets/images/artist-shape-02.png" alt="form_2">
        <div class="text_decoration">Events</div>
        <!-- /DECORATIONS -->

        <div class="container">
            <div class="row">
                <div class="col-10 offset-1">
                    <div>
                        <!-- TITLE -->
                        <div class="text-center title">
                            <h2>Artist coaching</h2>
                            <h3>Latest Online Courses</h3>
                        </div>
                        <!-- /TITLE -->

                        <!-- CARDS -->
                        <div class="row events_cardS">
                            <Card v-for="singleCard,index in cards" :key="index" class="col-12 col-md-6" :card="singleCard"/>
                        </div>
                        <!-- /CARDS -->
                    </div>
                </div>
            </div>
        </div>
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
                    title: 'The Acrylic Painting Accademy',
                    image: require('../assets/images/artist-course-08-480x480.jpg'),
                    subTitle: '$18.00',
                    classIcon1: 'far fa-file-alt',
                    classIcon2: 'fas fa-gamepad',
                    textIcon1: '4 Lessons',
                    textIcon2: '50 Students'
                },
                {
                    title: 'Drawing and Shading: Complete Course',
                    image: require('../assets/images/artist-course-07-480x480.jpg'),
                    subTitle: '$21.00',
                    classIcon1: 'far fa-file-alt',
                    classIcon2: 'fas fa-gamepad',
                    textIcon1: '14 Lessons',
                    textIcon2: '50 Students'
                },
                {
                    title: 'The Color Theory for Digital Artist',
                    image: require('../assets/images/artist-course-06-480x480.jpg'),
                    subTitle: '$19.00',
                    classIcon1: 'far fa-file-alt',
                    classIcon2: 'fas fa-gamepad',
                    textIcon1: '7 Lessons',
                    textIcon2: '50 Students'
                },
                {
                    title: 'Ultimate Guide to Digital Sketching for Beginner',
                    image: require('../assets/images/artist-course-05-480x480.jpg'),
                    subTitle: '$35.00',
                    classIcon1: 'far fa-file-alt',
                    classIcon2: 'fas fa-gamepad',
                    textIcon1: '14 Lessons',
                    textIcon2: '50 Students'
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

</style>