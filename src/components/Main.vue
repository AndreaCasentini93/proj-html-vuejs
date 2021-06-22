<template>
    <main>
        <!-- ARTIST COACHING -->
        <ArtistCoaching />
        <!-- /ARTIST COACHING -->

        <!-- CREATE LIKES -->
        <CreateLikes />
        <!-- /CREATE LIKES -->

        <!-- YOUTUBE -->
        <section>YOUTUBE</section>
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
import CreateLikes from './CreateLikes.vue';

export default {
    name: 'Main',
    components: {
        ArtistCoaching,
        CreateLikes
    }
}
</script>

<style lang="scss" scoped>
    @import '../assets/style/variables.scss';
    @import '../assets/style/mixins.scss';
</style>