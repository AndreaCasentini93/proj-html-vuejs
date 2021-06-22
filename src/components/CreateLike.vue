<template>
    <section>
        <div class="container">
            <div class="row">
                <div class="col-10 offset-1">
                    <div class="row">
                        <!-- COLUMN LEFT -->
                        <div class="col-12 col-md-6 text-center column_left">
                            <h3>I coach and mentor visual artists, like you, to Create Like You Mean It</h3>
                            <h2>Martin Garrix</h2>
                        </div>
                        <!-- /COLUMN LEFT -->

                        <!-- COLUMN RIGHT -->
                        <div class="col-12 col-md-6 column_right">
                            <p>
                                As a coach and menthor, my ultimate goal is to motivate visual artists toward inspirated action. I help you get you back on track to being the productive, creative, meaningful and authentic artist you truly want to be. I support artists in crafting and living a creative life as well as feeling good about themselves and their art.
                                <br>
                                <br>
                                As an artist and an educator for early 30 years, I understand what it takes to create.
                            </p>
                            <a href="#" class="btn_type_3">Get started today</a>
                        </div>
                        <!-- /COLUMN RIGHT -->
                    </div>
                </div>
            </div>
        </div>
    </section>
</template>

<script>
export default {
    name: 'CreateLike'
}
</script>

<style lang="scss" scoped>
    @import '../assets/style/variables.scss';
    @import '../assets/style/mixins.scss';

    section {
        padding-top: 40px;
        padding-bottom: 40px;
    }

    .column_left {
        padding: 0 40px;

        h2 {
            @include section-title-40px;
            margin-bottom: 40px;
        }

        h3 {
            line-height: 1.5;
            margin-bottom: 20px;
            font-size: 35px;
            font-weight: 700;
            color: $sub-title-color;
        }
    }

    p {
        margin-bottom: 50px;
        color: $base-color;
    }

    @media screen and (max-width: 991px) {
            div {
                h2 {
                    font-size: 30px !important;
                }

                h3 {
                    font-size: 20px !important;
                }

                p {
                    font-size: 14px !important;
                }
            }
        }
</style>