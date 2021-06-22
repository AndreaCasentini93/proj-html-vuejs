<template>
    <section class="position-relative">
        <!-- BACKGROUND DECORATIONS -->
        <svg xmlns="http://www.w3.org/2000/svg" width="200" height="202" fill="#FEF7F3" class="cloud hidden_1199px">
            <path class="elementor-shape-fill" d="M139.374 198.088c16.328 8.906 51.35-1.087 58.304-39.038 7.15-39.022-13.182-40.052-9.633-54.248 14.243-21.15 16.782-48.14 2.028-64.387-36.503-38.024-45.629 7.604-76.048-20.28C101.727 7.837 83.1-6.735 56.23 3.405 18.239 17.74 27.33 47.659 27.33 69.313c0 7.624-24.216 21.957-26.87 41.573-3.346 24.734 12.168 57.29 26.87 68.443 23.322 26.363 59.318 20.28 75.541 11.154 13.931-7.836 25.35 1.52 36.503 7.605z"/>
        </svg>
        <img v-for="image, index in images" :key="index" :class="image.name" :src="image.src" :alt="image.name">
        <!-- /BACKGROUND DECORATIONS -->

        <div class="container">
            <!-- TITLES -->
            <div class="text-center">
                <h2>Artist Coaching</h2>
                <h3>I understand what it takes to create.<br>I can help you with</h3>
            </div>
            <!-- /TITLES -->

            <!-- SERVICES -->
            <div class="row">
                <div class="col-10 offset-1">
                    <div class="row">
                        <div v-for="service, index in services" :key="index" class="col-12 col-md-6 col-lg-3 service_box">
                            <img :src="service.image" :alt="service.title">
                            <h4>{{ service.title }}</h4>
                            <p>{{ service.paragraph }}</p>
                        </div>
                    </div>
                </div>
            </div>
            <!-- /SERVICES -->
        </div>
    </section>
</template>

<script>
export default {
    name: 'ArtistCoaching',
    data: function() {
        return {
            images: [
                {
                    name: 'form_2',
                    src: require('../assets/images/artist-shape-01.png')
                },
                {
                    name: 'jagged_circle',
                    src: require('../assets/images/maxcoach-shape-13.png')
                },
                {
                    name: 'string',
                    src: require('../assets/images/maxcoach-shape-14.png')
                }
            ],
            services: [
                {
                    image: require('../assets/images/artist-box-image-01.png'),
                    title: 'Online Coures',
                    paragraph: 'Online art coaching now offers you a very powerfull way to redesignyour artist mind.'
                },
                {
                    image: require('../assets/images/artist-box-image-02.png'),
                    title: 'One to One',
                    paragraph: 'Getting the necessary calarity about the current state to halp you improve your ability.'
                },
                {
                    image: require('../assets/images/artist-box-image-03.png'),
                    title: 'Anywhere',
                    paragraph: 'Access to valuable and portable program which allow you to setup and live anywhere you want.'
                },
                {
                    image: require('../assets/images/artist-box-image-04.png'),
                    title: 'On Time',
                    paragraph: 'Punctuality is our top priority because it\'s an essential criteria to assess a program quality.'
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
        overflow: hidden;

        & > img {
            position: absolute;
            z-index: -1;
        }

        .cloud {
            position: absolute;
            top: 44%;
            right: 15%;
            transform: scale(1.5);
            z-index: -1;
        }

        .form_2 {
            top: 10%;
            left: -10%;
            transform: rotate(230deg);
            width: 570px;
        }

        .jagged_circle {
            top: 35%;
            right: -4%;
            width: 170px;
        }

        .string {
            top: 15%;
            width: 100vw;
        }

        .container {
            padding-top: 70px;
            padding-bottom: 90px;

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

            .service_box {
                img {
                    max-height: 90px;
                    max-width: 130px;
                    margin-bottom: 25px;
                    margin-top: 30px;
                }

                h4 {
                    margin-bottom: 15px;
                    font-size: 17px;
                    color: $sub-title-color;
                }

                p {
                    font-size: 14px;
                    color: $base-color;
                }
            }
        }

        @media screen and (max-width: 767px) {
            div {
                h2 {
                    font-size: 30px !important;
                }

                h3 {
                    font-size: 20px !important;
                }

                h4 {
                    font-size: 15px !important;
                }

                p {
                    font-size: 12px !important;
                }
            }
        }
    }
</style>