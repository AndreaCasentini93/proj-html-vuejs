<template>
    <main>
        <ArtistCoaching />
        <CreateLike />
        <Youtube />
        <Testimonials />
        <Courses />
        <Articles />
        <Events />
        <Newsletter @userEmail="enterEmail"/>
    </main>
</template>

<script>
import ArtistCoaching from './ArtistCoaching.vue';
import CreateLike from './CreateLike.vue';
import Youtube from './Youtube.vue';
import Testimonials from './Testimonials.vue';
import Courses from './Courses.vue';
import Articles from './Articles.vue';
import Events from './Events.vue';
import Newsletter from './Newsletter.vue';

export default {
    name: 'Main',
    components: {
        ArtistCoaching,
        CreateLike,
        Youtube,
        Testimonials,
        Courses,
        Articles,
        Events,
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