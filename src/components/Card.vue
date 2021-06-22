<template>
    <div class="single_card">
        Card
    </div>
</template>

<script>
export default {
    name: 'Card',
    props: {
        card: Object
    }
}
</script>

<style lang="scss" scoped>
    @import '../assets/style/variables.scss';
    @import '../assets/style/mixins.scss';

    // COURSES CARDS
    .courses_cards {

        .single_card {
            color: red;
        }

    }

</style>