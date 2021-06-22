<template>
    <div id="jumbotron" class="position-relative d-flex justify-content-center align-items-center">
        <!-- IMAGES -->
        <svg xmlns="http://www.w3.org/2000/svg" width="200" height="202" fill="#76CAF2" class="cloud_1 hidden_1199px">
            <path class="elementor-shape-fill" d="M139.374 198.088c16.328 8.906 51.35-1.087 58.304-39.038 7.15-39.022-13.182-40.052-9.633-54.248 14.243-21.15 16.782-48.14 2.028-64.387-36.503-38.024-45.629 7.604-76.048-20.28C101.727 7.837 83.1-6.735 56.23 3.405 18.239 17.74 27.33 47.659 27.33 69.313c0 7.624-24.216 21.957-26.87 41.573-3.346 24.734 12.168 57.29 26.87 68.443 23.322 26.363 59.318 20.28 75.541 11.154 13.931-7.836 25.35 1.52 36.503 7.605z"/>
        </svg>
        <svg xmlns="http://www.w3.org/2000/svg" width="200" height="202" fill="#F5C500" class="cloud_2 hidden_1199px">
            <path class="elementor-shape-fill" d="M139.374 198.088c16.328 8.906 51.35-1.087 58.304-39.038 7.15-39.022-13.182-40.052-9.633-54.248 14.243-21.15 16.782-48.14 2.028-64.387-36.503-38.024-45.629 7.604-76.048-20.28C101.727 7.837 83.1-6.735 56.23 3.405 18.239 17.74 27.33 47.659 27.33 69.313c0 7.624-24.216 21.957-26.87 41.573-3.346 24.734 12.168 57.29 26.87 68.443 23.322 26.363 59.318 20.28 75.541 11.154 13.931-7.836 25.35 1.52 36.503 7.605z"/>
        </svg>
        <img v-for="image, index in images" :key="index" :class="image.name + ' ' + image.class" :src="image.src" :alt="image.name">
        <!-- /IMAGES -->

        <!-- TEXT -->
        <div class="text-center">
            <h2>Hello, Im Matin</h2>
            <h3>Artist Coaching And Mentoring<br>Might Be For You</h3>
            <a href="#" class="btn_type_2">Get started today</a>
        </div>
        <!-- /TEXT -->
    </div>
</template>

<script>
export default {
    name: 'Jumbotron',
    data: function() {
        return {
            images: [
                {
                    name: 'form_1',
                    src: require('../assets/images/artist-shape-02.png'),
                    class: ''
                },
                {
                    name: 'form_2',
                    src: require('../assets/images/artist-shape-01.png'),
                    class: ''
                },
                {
                    name: 'feather',
                    src: require('../assets/images/artist-shape-04.png'),
                    class: ''
                },
                {
                    name: 'colors_1',
                    src: require('../assets/images/artist-shape-05.png'),
                    class: 'hidden_1199px'
                },
                {
                    name: 'photo',
                    src: require('../assets/images/artist-hero-image-04.jpg'),
                    class: 'hidden_1199px'
                },
                {
                    name: 'profile',
                    src: require('../assets/images/artist-hero-image-03.png'),
                    class: ''
                },
                {
                    name: 'points',
                    src: require('../assets/images/artist-shape-03.png'),
                    class: 'hidden_1199px'
                },
                {
                    name: 'colors_2',
                    src: require('../assets/images/artist-hero-image-02.jpg'),
                    class: 'hidden_1199px'
                },
                {
                    name: 'monkey',
                    src: require('../assets/images/artist-hero-image-01.jpg'),
                    class: 'hidden_1199px'
                }
            ]
        }
    }
}
</script>

<style lang="scss" scoped>
    @import '../assets/style/variables.scss';
    @import '../assets/style/mixins.scss';

    #jumbotron {
        height: 600px;
        background-color: $bg-jumbotron;
        overflow: hidden;

        img {
            position: absolute;
        }

        .cloud_1 {
            position: absolute;
            top: 40%;
            left: 3%;
            transform: scale(2);
        }

        .cloud_2 {
            position: absolute;
            right: 23%;
            bottom: 10%;
            transform: scale(0.8);
        }

        .form_1 {
            top: 0;
            left: 0;
            width: 700px;
        }
        
        .form_2 {
            right: 10%;
            width: 540px;
        }

        .photo {
            right: 15%;
            bottom: 9%;
            width: 260px;
            box-shadow: 0 0 25px 1px lighten($base-color, 30%);
        }

        .profile {
            bottom: 2%;
            left: 26%;
            width: 200px;
        }

        .monkey {
            bottom: 11%;
            left: 8%;
            width: 150px;
            box-shadow: 0 0 25px 1px lighten($base-color, 30%);
        }

        .points {
            bottom: 10%;
            left: 0;
            width: 282px;
        }

        .feather {
            right: 11%;
            bottom: 48%;
            width: 100px;
        }

        .colors_1 {
            right: 7%;
            bottom: 0;
            width: 270px;
        }

        .colors_2 {
            bottom: 37%;
            left: 17%;
            width: 240px;
            box-shadow: 0 0 25px 1px lighten($base-color, 30%);
        }

        div {
            z-index: 1;
            h2 {
                @include section-title-40px;
            }

            h3 {
                line-height: 1.5;
                margin-bottom: 50px;
                font-size: 28px;
                font-weight: 700;
                color: $sub-title-color;
            }
        }

        @media screen and (max-width: 1355px) {

            .cloud {
                transform: scale(1.5);
            }

            .form_1 {
                width: 660px;
            }
            
            .form_2 {
                width: 500px;
            }

            .photo {
                width: 220px;
            }

            .profile {
                width: 160px;
            }

            .monkey {
                width: 140px;
            }

            .points {
                width: 242px;
            }

            .feather {
                width: 60px;
            }

            .colors_1 {
                width: 230px;
            }

            .colors_2 {
                width: 200px;
            }
        }
        @media screen and (max-width: 1199px) {
            .hidden_1199px {
                display: none !important;
            }
        }
        @media screen and (max-width: 767px) {
            div {
                h2 {
                    font-size: 30px;
                }

                h3 {
                    font-size: 20px;
                }
            }
        }
    }
</style>