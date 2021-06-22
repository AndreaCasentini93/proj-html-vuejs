<template>
    <section>
        <!-- DECORATIONS -->
        
        <!-- /DECORATIONS -->

        <!-- TITLE -->
        <div class="text-center">
            <h2>Artist coaching</h2>
            <h3>Latest Online Courses</h3>
        </div>
        <!-- /TITLE -->

        <!-- CARDS -->

        <!-- /CARDS -->

        <!-- BUTTON -->
        <div class="text-center">
            <a href="#" class="btn_type_3">View all courses <i class="fas fa-long-arrow-alt-right"></i></a>
        </div>
        <!-- /BUTTON -->
    </section>
</template>

<script>
export default {
    name: 'Courses'
}
</script>

<style lang="scss" scoped>
    @import '../assets/style/variables.scss';
    @import '../assets/style/mixins.scss';

    section {
        padding: 50px 0;

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