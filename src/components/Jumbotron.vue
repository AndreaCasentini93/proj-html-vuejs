<template>
    <div id="jumbotron" class="position-relative">
        <img class="artist-shape-02" src="../assets/images/artist-shape-02.png" alt="artist-shape-02">
        <img class="artist-shape-01" src="../assets/images/artist-shape-01.png" alt="artist-shape-01">
        <img class="artist-hero-image-04" src="../assets/images/artist-hero-image-04.jpg" alt="artist-hero-image-04">
        <img class="artist-hero-image-03" src="../assets/images/artist-hero-image-03.png" alt="artist-hero-image-03">
        <img class="artist-shape-03" src="../assets/images/artist-shape-03.png" alt="artist-shape-03">
        <img class="artist-hero-image-01" src="../assets/images/artist-hero-image-01.jpg" alt="artist-hero-image-01">
        <img class="artist-shape-04" src="../assets/images/artist-shape-04.png" alt="artist-shape-04">
        <!-- <img class="artist-shape-05" src="../assets/images/artist-shape-05.png" alt="artist-shape-05">
        <img class="artist-hero-image-02" src="../assets/images/artist-hero-image-02.jpg" alt="artist-hero-image-02"> -->
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

        .artist-shape-02 {
            left: 0;
            width: 700px;
        }
        
        .artist-shape-01 {
            right: 10%;
            width: 580px;
        }

        .artist-hero-image-04 {
            bottom: 8%;
            right: 15%;
            width: 260px;
        }

        .artist-hero-image-03 {
            bottom: 2%;
            left: 26%;
            width: 200px;
        }

        .artist-hero-image-01 {
            bottom: 8%;
            left: 8%;
            width: 150px;
            box-shadow: 0 0 25px 1px lighten($base-color, 20%);
        }

        .artist-shape-03 {
            left: 0;
            bottom: 10%;
            width: 282px;
        }
    }
</style>