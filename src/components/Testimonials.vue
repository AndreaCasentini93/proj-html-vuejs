<template>
    <section>
        <div class="container">
            <!-- TITLES -->
            <div class="text-center">
                <h2>Testimonials</h2>
                <h3>Why do people love me?</h3>
            </div>
            <!-- /TITLES -->

            <!-- SLIDER -->
            <div class="slider">
                
            </div>
            <!-- SLIDER -->
        </div>
    </section>
</template>

<script>
export default {
    name: 'Testimonials'
}
</script>

<style lang="scss" scoped>
    @import '../assets/style/variables.scss';
    @import '../assets/style/mixins.scss';

    section {
        padding: 30px 0;
        background-color: $bg-testimonials;

        div {

            h2 {
                @include section-title-35px;
            }

            h3 {
                line-height: 1.2;
                margin-bottom: 50px;
                font-size: 25px;
                font-weight: 700;
                color: $sub-title-color;
            }
        }
    }
</style>