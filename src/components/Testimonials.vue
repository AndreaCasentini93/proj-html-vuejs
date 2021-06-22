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
            <div class="d-flex slider">
                <!-- BEFORE SLIDE -->
                <div class="slide" @click="changeSlide(slides[beforeId].id)">
                    <h4>{{ slides[beforeId].title }}</h4>
                    <p>{{ slides[beforeId].text }}</p>
                    <div class="d-flex">
                        <img :src="slides[beforeId].avatarImage" :alt="slides[beforeId].avatarName">
                        <div>
                            <h5>{{ slides[beforeId].avatarName }}</h5>
                            <h6>{{ slides[beforeId].avatarTask }}</h6>
                        </div>
                    </div>
                </div>
                <!-- /BEFORE SLIDE -->

                <!-- CURRENT SLIDE -->
                <div class="slide">
                    <h4>{{ slides[currentId].title }}</h4>
                    <p>{{ slides[currentId].text }}</p>
                    <div class="d-flex">
                        <img :src="slides[currentId].avatarImage" :alt="slides[currentId].avatarName">
                        <div>
                            <h5>{{ slides[currentId].avatarName }}</h5>
                            <h6>{{ slides[currentId].avatarTask }}</h6>
                        </div>
                    </div>
                </div>
                <!-- /CURRENT SLIDE -->

                <!-- AFTER SLIDE -->
                <div class="slide" @click="changeSlide(slides[afterId].id)">
                    <h4>{{ slides[afterId].title }}</h4>
                    <p>{{ slides[afterId].text }}</p>
                    <div class="d-flex">
                        <img :src="slides[afterId].avatarImage" :alt="slides[afterId].avatarName">
                        <div>
                            <h5>{{ slides[afterId].avatarName }}</h5>
                            <h6>{{ slides[afterId].avatarTask }}</h6>
                        </div>
                    </div>
                </div>
                <!-- /AFTER SLIDE -->
            </div>
            <!-- SLIDER -->

            <!-- CIRCLE -->
            <div class="text-center circle_box">
                <i v-for="slide in slides" :key="slide.id" :class="slide.id == currentId? 'active':'' " class="fas fa-circle" @click="changeSlide(slide.id)"></i>
            </div>
            <!-- /CIRCLE -->
        </div>
    </section>
</template>

<script>
export default {
    name: 'Testimonials',
    data: function() {
        return {
            slides: [
                {
                    id: 0,
                    title: 'Height level of efficiency and scientific teaching methods',
                    text: 'I am free to learn at my own pace, follow my own schedule and choose the subject I want to learn from the syllabus. Great study portal for peaple like me.',
                    avatarImage: require('../assets/images/artist-testimonial-avatar-04.jpg'),
                    avatarName: 'Mina Hollace',
                    avatarTask: '/ FreeLancer'
                },
                {
                    id: 1,
                    title: 'Professional team of specialists and appassionate mentors at reach',
                    text: 'I need to get a certification for English proficiency and MaxCoach is my best choice. Their tutors are smart and professional when dealing with students.',
                    avatarImage: require('../assets/images/artist-testimonial-avatar-01.jpg'),
                    avatarName: 'Madley Pondor',
                    avatarTask: '/ IT Specialist'
                },
                {
                    id: 2,
                    title: 'It\'s a choice of quality for people with special need',
                    text: 'I\'m a very strict person so I require everything to be organized and neat. Then, I\'ll be able to make things right and shine. MaxCoach guys just got me.',
                    avatarImage: require('../assets/images/artist-testimonial-avatar-02.jpg'),
                    avatarName: 'Florence Themes',
                    avatarTask: '/ Multimedia Admin'
                }
            ],
            currentId: 0,
            afterId: 1,
            beforeId: 2
        }
    },
    methods: {
        changeSlide: function(id) {
            this.currentId = id;
            console.log('Corrente', this.currentId);
            if (id + 1 > this.slides.length - 1) {
                this.afterId = 0;
            } else {
                this.afterId = id + 1;
            }
            console.log('After', this.afterId);
            if (this.afterId + 1 > this.slides.length - 1) {
                this.beforeId = 0;
            } else {
                this.beforeId = this.afterId + 1;
            }
            console.log('Before', this.beforeId);
        }
    }
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
                margin-bottom: 40px;
                font-size: 25px;
                font-weight: 700;
                color: $sub-title-color;
            }
        }

        .slider {
            .slide {
                width: calc((100% / 3) - 40px);
                padding: 35px;
                border-radius: 5px;
                margin: 0 20px;
                background-color: #FFFFFF;
                cursor: pointer;
                @include transition-type-1(transform);

                &:first-of-type,
                &:last-of-type {
                    opacity: .5;
                }

                &:hover {
                    transform: scale(1.05);
                }

                h4 {
                    line-height: 1.8;
                    font-size: 14.5px;
                    font-weight: 700;
                    color: $sub-title-color;
                }

                p {
                    margin-bottom: 35px;
                    font-size: 14px;
                    color: $base-color;
                }

                img {
                    width: 60px;
                    border-radius: 50%;
                    margin-right: 25px;
                }

                h5 {
                    font-size: 13px;
                    font-weight: 700;
                    color: $sub-title-color;
                }

                h6 {
                    font-size: 13px;
                    color: $base-color;
                }
            }
        }

        .circle_box {
            margin-top: 20px;

            i {
                font-size: 6px;
                margin: 0 5px;
                cursor: pointer;
                opacity: .3;
                @include transition-type-1(font-sixe);
                @include transition-type-1(opacity);


                &:hover,
                &.active {
                    font-size: 8px;
                    opacity: 1;
                }
            }
        }
    }
</style>