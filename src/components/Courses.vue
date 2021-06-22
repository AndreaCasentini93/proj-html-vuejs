<template>
    <section class="position-relative">
        <!-- DECORATIONS -->
        <img class="form_2_1" src="../assets/images/artist-shape-01.png" alt="form_2">
        <img class="form_2_2" src="../assets/images/artist-shape-01.png" alt="form_2">
        <div class="text_decoration hidden_991px">Courses</div>
        <!-- /DECORATIONS -->

        <div class="container">
            <!-- TITLE -->
            <div class="text-center">
                <h2>Artist coaching</h2>
                <h3>Latest Online Courses</h3>
            </div>
            <!-- /TITLE -->

            <!-- CARDS -->
            <div class="row courses_cards">
                <Card v-for="card,index in cards" :key="index" class="col-12 col-md-6 col-lg-3" :card="sindleCard"/>
            </div>
            <!-- /CARDS -->

            <!-- BUTTON -->
            <div class="text-center">
                <a href="#" class="btn_type_3">View all courses <i class="fas fa-long-arrow-alt-right"></i></a>
            </div>
            <!-- /BUTTON -->
        </div>
    </section>
</template>

<script>
import Card from './Card.vue';

export default {
    name: 'Courses',
    components: {
        Card
    },
    data: function() {
        return {
            cards: [
                {
                    title: 'The Acrylic Painting Accademy',
                    image: require('../assets/images/artist-course-08-480x480.jpg'),
                    price: '&#x24;18.00',
                    classIcon1: 'far fa-file-alt',
                    classIcon2: 'fas fa-gamepad',
                },
                {
                    title: 'Drawing and Shading: Complete Course',
                    image: require('../assets/images/artist-course-07-480x480.jpg'),
                    price: '&#x24;21.00',
                    classIcon1: 'far fa-file-alt',
                    classIcon2: 'fas fa-gamepad',
                },
                {
                    title: 'The Color Theory for Digital Artist',
                    image: require('../assets/images/artist-course-06-480x480.jpg'),
                    price: '&#x24;19.00',
                    classIcon1: 'far fa-file-alt',
                    classIcon2: 'fas fa-gamepad',
                },
                {
                    title: 'Ultimate Guide to Digital Sketching for Beginner',
                    image: require('../assets/images/artist-course-05-480x480.jpg'),
                    price: '&#x24;35.00',
                    classIcon1: 'far fa-file-alt',
                    classIcon2: 'fas fa-gamepad',
                },
                {
                    title: 'Portrait Drawing The Smart Way',
                    image: require('../assets/images/artist-course-04-480x480.jpg'),
                    price: '&#x24;19.00',
                    classIcon1: 'far fa-file-alt',
                    classIcon2: 'fas fa-gamepad',
                },
                {
                    title: 'Mastering Watercolor Painting from Beginner',
                    image: require('../assets/images/artist-course-03-480x480.jpg'),
                    price: '&#x24;19.00',
                    classIcon1: 'far fa-file-alt',
                    classIcon2: 'fas fa-gamepad',
                },
                {
                    title: 'The Artist & Science of Drawing',
                    image: require('../assets/images/artist-course-02-480x480.jpg'),
                    price: '&#x24;25.00',
                    classIcon1: 'far fa-file-alt',
                    classIcon2: 'fas fa-gamepad',
                },
                {
                    title: 'The Colored Pencil Drawing Course',
                    image: require('../assets/images/artist-course-01-480x480.jpg'),
                    price: '&#x24;22.00',
                    classIcon1: 'far fa-file-alt',
                    classIcon2: 'fas fa-gamepad',
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
        padding: 50px 0;
        overflow: hidden;

        & > img {
            position: absolute;
            width: 400px;
        }

        .text_decoration {
            position: absolute;
            top: 55%;
            right: -8%;
            text-transform: uppercase;
            font-size: 100px;
            font-family: $decoration-font;
            color: lighten($ashtag-color, 30%);
            transform: rotate(90deg);
        }

        .form_2_1 {
            bottom: 0;
            left: -15%;
            filter: invert(100%) brightness(150%);
            transform: rotate(10deg);
        }

        .form_2_2 {
            top: 25%;
            right: -15%;
            transform: rotate(250deg);
        }

        div {
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

        div {
            .btn_type_3 {
                i {
                    vertical-align: middle;
                }
            }
        }
    }

    @media screen and (max-width: 991px) {
        
        .hidden_991px {
            display: none !important;
        }

    }
</style>