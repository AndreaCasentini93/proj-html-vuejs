<template>
    <section class="position-relative">
        <!-- DECORATIONS -->
        <img class="form_2_1" src="../assets/images/artist-shape-01.png" alt="form_2">
        <img class="form_2_2" src="../assets/images/artist-shape-01.png" alt="form_2">
        <!-- /DECORATIONS -->

        <div class="container">
            <!-- TITLE -->
            <div class="text-center">
                <h2>Artist coaching</h2>
                <h3>Latest Online Courses</h3>
            </div>
            <!-- /TITLE -->

            <!-- CARDS -->
            <Card />
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
</style>