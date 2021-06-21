<template>
    <ul class="d-flex align-items-center menu_socials hidden_1199px">
        <li v-for="social, index in menuSocials" :key="index" class="d-flex align-items-center">
            <a :href="social.url" class="social_link">
                <i :class="social.class"></i>
            </a>
        </li>
    </ul>
</template>

<script>
export default {
    name: 'Social',
    props: {
        menuSocials: Array
    }
}
</script>

<style lang="scss" scoped>
    @import '../assets/style/variables.scss';
    @import '../assets/style/mixins.scss';

    .social_link {
        @include menu-social-media;
    }
</style>