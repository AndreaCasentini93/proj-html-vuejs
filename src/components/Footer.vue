<template>
    <footer>
        <div class="container">
            footer
        </div>
    </footer>
</template>

<script>
export default {
    name: 'Footer',
    props: {
        socials: Array,
        explore: Array,
        information: Array
    }
}
</script>

<style lang="scss" scoped>
    @import '../assets/style/variables.scss';
    @import '../assets/style/mixins.scss';

</style>