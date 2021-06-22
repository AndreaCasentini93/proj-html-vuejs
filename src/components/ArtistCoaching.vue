<template>
    <section class="position-relative">
        <img v-for="image, index in images" :key="index" :class="image.name" :src="image.src" :alt="image.name">
        <div class="container">
            <!-- TITLES -->
            <div class="text-center">
                <h2>Hello, Im Matin</h2>
                <h3>Artist Coaching And Mentoring<br>Might Be For You</h3>
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

        .form_2 {
            top: 10%;
            left: -5%;
            transform: rotate(230deg);
            width: 450px;
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
    }
</style>