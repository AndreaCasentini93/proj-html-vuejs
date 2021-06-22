<template>
    <section>
        <!-- DECORATIONS -->
        <img v-for="n in 2" :key="n" class="dotted_circle" src="../assets/images/maxcoach-shape-05.png" alt="dotted_circle">
        <!-- /DECORATIONS -->
    </section>
</template>

<script>
export default {
    name: 'Youtube',
}
</script>

<style lang="scss" scoped>
    @import '../assets/style/variables.scss';
    @import '../assets/style/mixins.scss';

</style>