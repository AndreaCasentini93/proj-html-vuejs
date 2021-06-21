<template>
    <header>
        <!-- COUNTDOWN -->
        <Countdown />
        <!-- /COUNTDOWN -->

        <!-- MENU -->
        <Menu :menuLinks="links" :menuSocials="socials"/>
        <!-- /MENU -->

        <!-- JUMBOTRON -->
        <Jumbotron />
        <!-- /JUMBOTRON -->
    </header>
</template>

<script>
import Countdown from './Countdown.vue';
import Menu from './Menu.vue';
import Jumbotron from './Jumbotron.vue';

export default {
    name: 'Header',
    props: {
        links: Array,
        socials: Array
    },
    components: {
        Countdown,
        Menu,
        Jumbotron
    }
}
</script>

<style lang="scss" scoped>
    @import '../assets/style/variables.scss';
    @import '../assets/style/mixins.scss';

</style>