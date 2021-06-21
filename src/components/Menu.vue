<template>
    <nav>
        <div class="position-relative d-flex justify-content-between align-items-center container">
            <!-- LOGO -->
            <a href="#">
                <img src="../assets/images/dark-logo.png" alt="Logo MaxCoach">
            </a>
            <!-- /LOGO -->

            <!-- LINKS MENU -->
            <ul class="d-flex align-items-center hidden_1199px">
                <li v-for="link, index in menuLinks" :key="index" class="d-flex align-items-center links_in_menu">
                    <a :href="link.url" class="menu_link">{{ link.text }} <i v-if="link.dropdowns" class="fas fa-chevron-down"></i></a>
                </li>
            </ul>
            <!-- /LINKS MENU -->

            <!-- SOCIAL MENU -->
            <Socials :menuSocials="menuSocials"/>
            <!-- /SOCIAL MENU -->

            <!-- DROPDOWN MENU-->
            <i class="fas fa-bars" @click.prevent="!openMenu? openMenu = true: openMenu = false"></i>
            <div v-if="openMenu" class="dropdown_menu">
                <ul>
                    <li v-for="link, index in menuLinks" :key="index">
                        <a :href="link.url" class="menu_link">{{ link.text }} <i v-if="link.dropdowns" class="fas fa-chevron-down"></i></a>
                    </li>
                    <li v-for="social, index in menuSocials" :key="index" class="d-inline-block">
                        <a :href="social.url" class="social_link">
                            <i :class="social.class"></i>
                        </a>
                    </li>
                </ul>
            </div>
            <!-- /DROPDOWN MENU-->
        </div>
    </nav>
</template>

<script>
import Socials from './Socials.vue';

export default {
    name: 'Menu',
    props: {
        menuLinks: Array,
        menuSocials: Array
    },
    components: {
        Socials
    },
    data: function() {
        return {
            openMenu: false
        }
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

            .fas.fa-bars {
                display: none;
                font-size: 25px;
            }

            .dropdown_menu {
                display: none;
                position: absolute;
                bottom: -360%;
                right: 10px;
                width: 200px;
                min-height: 320px;
                background-color: white;
                z-index: 2;

                & > ul > li {
                    margin: 15px 10px;
                }
            }

            @media screen and (max-width: 1199px) {
                .hidden_1199px {
                    display: none !important;
                }

                .fas.fa-bars {
                    display: block;
                }

                .dropdown_menu {
                    display: block;

                    ul {
                        li.d-inline-block {
                            margin: 15px 2px;
                        }
                    }
                }
            }
        }
    }

</style>