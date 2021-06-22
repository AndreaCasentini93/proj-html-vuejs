<template>
    <div id="jumbotron" class="position-relative d-flex justify-content-center align-items-center">
        <!-- IMAGES -->
        <img v-for="image, index in images" :key="index" :class="image.name" :src="image.src" :alt="image.name" class="hidden_1199px">
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
                    src: require('../assets/images/artist-shape-02.png')
                },
                {
                    name: 'form_2',
                    src: require('../assets/images/artist-shape-01.png')
                },
                {
                    name: 'feather',
                    src: require('../assets/images/artist-shape-04.png')
                },
                {
                    name: 'colors_1',
                    src: require('../assets/images/artist-shape-05.png')
                },
                {
                    name: 'photo',
                    src: require('../assets/images/artist-hero-image-04.jpg')
                },
                {
                    name: 'profile',
                    src: require('../assets/images/artist-hero-image-03.png')
                },
                {
                    name: 'points',
                    src: require('../assets/images/artist-shape-03.png')
                },
                {
                    name: 'colors_2',
                    src: require('../assets/images/artist-hero-image-02.jpg')
                },
                {
                    name: 'monkey',
                    src: require('../assets/images/artist-hero-image-01.jpg')
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