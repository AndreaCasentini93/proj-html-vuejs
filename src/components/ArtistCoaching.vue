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
            <div class="d-flex flex-wrap services_box">
                <div>ciao</div>
                <div>ciao</div>
                <div>ciao</div>
                <div>ciao</div>
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
            ]
        }
    }
}
</script>

<style lang="scss" scoped>
    @import '../assets/style/variables.scss';
    @import '../assets/style/mixins.scss';

    section {
        height: 500px;
        overflow: hidden;

        img {
            position: absolute;
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

            .services_box {
                padding: 0 150px;

                div {
                    width: calc((100% / 4) - 40px);
                    margin: 0 20px;
                }
            }
        }
    }
</style>