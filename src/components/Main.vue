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
        <section>ONLINE COURSES</section>
        <!-- /COURSES -->

        <!-- ARTICLES -->
        <section>ARTICLES</section>
        <!-- /ARTICLES -->

        <!-- EVENTS -->
        <section>EVENTS</section>
        <!-- /EVENTS -->

        <!-- NEWSLETTER -->
        <section>NEWSLETTER</section>
        <!-- /NEWSLETTER -->
    </main>
</template>

<script>
import ArtistCoaching from './ArtistCoaching.vue';
import CreateLike from './CreateLike.vue';
import Youtube from './Youtube.vue';
import Testimonials from './Testimonials.vue';

export default {
    name: 'Main',
    components: {
        ArtistCoaching,
        CreateLike,
        Youtube,
        Testimonials
    }
}
</script>

<style lang="scss" scoped>
    @import '../assets/style/variables.scss';
    @import '../assets/style/mixins.scss';
</style>