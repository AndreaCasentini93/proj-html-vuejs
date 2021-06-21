<template>
    <div id="jumbotron" class="position-relative d-flex justify-content-center align-items-center">
        <!-- IMAGES -->
        <img class="form_1" src="../assets/images/artist-shape-02.png" alt="form_1">
        <img class="form_2" src="../assets/images/artist-shape-01.png" alt="form_2">
        <img class="feather" src="../assets/images/artist-shape-04.png" alt="feather">
        <img class="colors_1" src="../assets/images/artist-shape-05.png" alt="colors_1">
        <img class="photo" src="../assets/images/artist-hero-image-04.jpg" alt="photo">
        <img class="profile" src="../assets/images/artist-hero-image-03.png" alt="profile">
        <img class="points" src="../assets/images/artist-shape-03.png" alt="points">
        <img class="colors_2" src="../assets/images/artist-hero-image-02.jpg" alt="colors_2">
        <img class="monkey" src="../assets/images/artist-hero-image-01.jpg" alt="monkey">
        <!-- /IMAGES -->

        <!-- TEXT -->
        <div class="text-center">
            <h2>Hello, Im Matin</h2>
            <h3>Artist Coaching And Mentoring<br>Might Be For You</h3>
        </div>
        <!-- /TEXT -->
    </div>
</template>

<script>
export default {
    name: 'Jumbotron'
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
                @include section-title;
            }

            h3 {
                line-height: 1.5;
                font-size: 31px;
                font-weight: 700;
                color: $sub-title-color;
            }
        }
    }
</style>