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
        <section>TESTIMONIALS</section>
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

export default {
    name: 'Main',
    components: {
        ArtistCoaching,
        CreateLike,
        Youtube
    }
}
</script>

<style lang="scss" scoped>
    @import '../assets/style/variables.scss';
    @import '../assets/style/mixins.scss';
</style>