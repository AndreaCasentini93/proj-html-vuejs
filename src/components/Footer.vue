<template>
    <footer>
        <div class="container">
            <div class="row">
                <!-- COLUMN 1 -->
                <div class="col-12 col-md-8 col-lg-4">
                    <h4>Address</h4>
                    <ul>
                        <li>
                            {{ contacts.address }}
                        </li>
                        <li>
                            {{ contacts.phone }}
                        </li>
                        <li>
                            {{ contacts.email }}
                        </li>
                    </ul>
                    <Socials :menuSocials="socials"/>
                </div>
                <!-- /COLUMN 1 -->

                <!-- COLUMN 2 -->
                <div class="col-12 col-md-4 col-lg-2">
                    <h4>Explore</h4>
                    <ul>
                        <li v-for="link, index in explore" :key="index">
                            <a :href="link.url">{{ link.text }}</a>
                        </li>
                    </ul>
                </div>
                <!-- /COLUMN 2 -->

                <!-- COLUMN 3 -->
                <div class="col-12 col-md-4 col-lg-2">
                    <h4>Information</h4>
                    <ul>
                        <li v-for="link, index in information" :key="index">
                            <a :href="link.url">{{ link.text }}</a>
                        </li>
                    </ul>
                </div>
                <!-- /COLUMN 3 -->

                <!-- COLUMN 4 -->
                <div class="col-12 col-md-8 col-lg-4">
                    <h4>Instagram <span class="ashtag">@maxcoach</span></h4>
                    <ul class="d-flex flex-wrap">
                        <li v-for="image, index in images" :key="index">
                            <a :href="image.url">
                                <img :src="image.src" :alt="image.alt">
                            </a>
                        </li>
                    </ul>
                </div>
                <!-- /COLUMN 4 -->

                <!-- RESERVED -->
                <p class="col-12 text-center">&#xa9; 2020 Maxcoach. All Rights Reserved</p>
                <!-- /RESERVED -->
            </div>
        </div>
    </footer>
</template>

<script>
import Socials from './Socials.vue';

export default {
    name: 'Footer',
    props: {
        socials: Array,
        contacts: Object,
        explore: Array,
        information: Array
    },
    components: {
        Socials
    },
    data: function() {
        return {
            images: [
                {
                    src: require('../assets/images/120084500_197897808368764_8114555493043279565_n.jpg'),
                    alt: 'Image Artists 1',
                    url: '#'
                },
                {
                    src: require('../assets/images/120012142_177596140500760_8623485824101406058_n.jpg'),
                    alt: 'Image Artists 2',
                    url: '#'
                },
                {
                    src: require('../assets/images/120099363_364334431619755_7198812647386067017_n.jpg'),
                    alt: 'Image Artists 3',
                    url: '#'
                }
            ]
        }
    }
}
</script>

<style lang="scss" scoped>
    @import '../assets/style/variables.scss';
    @import '../assets/style/mixins.scss';

    footer {
        .container {
            padding-top: 90px;
            padding-bottom: 20px;

            .row {
                div {

                    &:not(:last-of-type) {
                        margin-bottom: 50px;
                    }

                    h4 {
                        margin-bottom: 10px;
                        font-size: 17px;
                        font-weight: 700;
                        color: $sub-title-color;

                        .ashtag {
                            font-size: 15px;
                            color: $ashtag-color;
                        }
                    }

                    ul {
                        li {
                            margin-bottom: 15px;
                            font-size: 14px;
                            color: $base-color;

                            a {
                                font-size: 14px;
                                color: $base-color;
                                @include transition-type-1(color);

                                &:hover {
                                    color: darken($link-color, 20%);
                                }

                                img {
                                    max-width: 100px;
                                    margin-top: 20px;
                                    margin-right: 20px;
                                    @include transition-type-1(opacity);

                                    &:hover {
                                        opacity: .8;
                                    }
                                }
                            }
                        }
                    }
                }

                p {
                    font-size: 14px;
                    color: $base-color;
                }
            }
        }
        @media screen and (max-width: 767px) {
            h4 {
                font-size: 15px !important;
            }
            .ashtag {
                font-size: 14px !important;
            }
            li {
                font-size: 12px !important;
            }
            a {
                font-size: 12px !important;
            }
            p {
                font-size: 12px !important;
            }
        }
    }
</style>