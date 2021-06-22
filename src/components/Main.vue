<template>
    <main>
        <!-- ARTIST COACHING -->
        <ArtistCoaching />
        <!-- /ARTIST COACHING -->

        <!-- CREATE LIKES -->
        <CreateLike />
        <!-- /CREATE LIKES -->

        <!-- YOUTUBE -->
        <Youtube />
        <!-- /YOUTUBE -->

        <!-- TESTIMONIALS -->
        <Testimonials />
        <!-- /TESTIMONIALS -->

        <!-- COURSES -->
        <Courses />
        <!-- /COURSES -->

        <!-- ARTICLES -->
        <section>ARTICLES</section>
        <!-- /ARTICLES -->

        <!-- EVENTS -->
        <section>EVENTS</section>
        <!-- /EVENTS -->

        <!-- NEWSLETTER -->
        <Newsletter @userEmail="enterEmail"/>
        <!-- /NEWSLETTER -->
    </main>
</template>

<script>
import ArtistCoaching from './ArtistCoaching.vue';
import CreateLike from './CreateLike.vue';
import Youtube from './Youtube.vue';
import Testimonials from './Testimonials.vue';
import Courses from './Courses.vue';
import Newsletter from './Newsletter.vue';

export default {
    name: 'Main',
    components: {
        ArtistCoaching,
        CreateLike,
        Youtube,
        Testimonials,
        Courses,
        Newsletter
    },
    data: function() {
        return {
            clientEmail: ''
        }
    },
    methods: {
        enterEmail: function(val) {
            this.clientEmail = val;
            this.$emit('userEmail', this.clientEmail);
        }
    }
}
</script>

<style lang="scss" scoped>
    @import '../assets/style/variables.scss';
    @import '../assets/style/mixins.scss';
</style>