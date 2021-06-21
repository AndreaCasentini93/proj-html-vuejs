<template>
    <nav>
        <div class="d-flex justify-content-between align-items-center container">
            <a href="#">
                <img src="../assets/images/dark-logo.png" alt="Logo MaxCoach">
            </a>
            <ul class="d-flex align-items-center">
                <li v-for="link, index in menuLinks" :key="index" class="d-flex align-items-center links_in_menu">
                    <a :href="link.url" class="menu_link">{{ link.text }} <i v-if="link.dropdowns" class="fas fa-chevron-down"></i></a>
                </li>
            </ul>
            <ul class="d-flex align-items-center menu_socials">
                <li v-for="social, index in menuSocials" :key="index" class="d-flex align-items-center">
                    <a :href="social.url" class="social_link">
                        <i :class="social.class"></i>
                    </a>
                </li>
            </ul>
        </div>
    </nav>
</template>

<script>
export default {
    name: 'Menu',
    props: {
        menuLinks: Array,
        menuSocials: Array
    }
}
</script>

<style lang="scss" scoped>
    @import '../assets/style/variables.scss';
    @import '../assets/style/mixins.scss';

    nav {
        height: 90px;

        div {
            height: 100%;

            a {
                img {
                    width: 150px;
                }
            }

            ul {
                height: 100%;

                li {
                    &.links_in_menu {
                        height: 100%;
                        margin: 0 15px;
                        border-bottom: 2px solid $invisible-color;
                        @include transition-type-1(border-bottom);
                    }

                    &.links_in_menu:hover,
                    &.links_in_menu.active {
                        border-bottom: 2px solid lighten($link-color, 45%);
                    }

                    a {
                        .fas.fa-chevron-down {
                            margin-left: 3px;
                            vertical-align: middle;
                            font-size: 10px;
                        }
                    }

                    .menu_link {
                        font-size: 14px;
                        color: $link-color;
                        @include transition-type-1(color);

                        &:hover {
                            color: lighten($link-color, 45%);
                        }
                    }

                    .social_link {
                        @include menu-social-media;
                    }
                }
            }
        }
    }

</style>