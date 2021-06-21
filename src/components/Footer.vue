<template>
    <footer>
        <div class="container">
            <div class="row">
                <!-- COLUMN 1 -->
                <div class="col-12 col-md-8 col-lg-4">
                    <h4>Address</h4>
                    <ul>
                        <li>
                            {{ contacts.adress }}
                        </li>
                        <li>
                            {{ contacts.phone }}
                        </li>
                        <li>
                            {{ contacts.email }}
                        </li>
                    </ul>
                    <ul class="d-flex align-items-center menu_socials">
                        <li v-for="social, index in socials" :key="index" class="d-flex align-items-center">
                            <a :href="social.url" class="social_link">
                                <i :class="social.class"></i>
                            </a>
                        </li>
                    </ul>
                </div>
                <!-- /COLUMN 1 -->

                <!-- COLUMN 2 -->
                <div class="col-12 col-md-4 col-lg-2">
                    <h4>Address</h4>
                    <ul>
                        <li v-for="link, index in explore" :key="index">
                            <a :href="link.url">{{ link.text }}</a>
                        </li>
                    </ul>
                </div>
                <!-- /COLUMN 2 -->

                <!-- COLUMN 3 -->
                <div class="col-12 col-md-4 col-lg-2">
                    <h4>Address</h4>
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

                <div class="col-12 text-center">&#xa9; 2020 Maxcoach. All Rights Reserved</div>
            </div>
        </div>
    </footer>
</template>

<script>
export default {
    name: 'Footer',
    props: {
        socials: Array,
        contacts: Object,
        explore: Array,
        information: Array
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
            padding-top: 50px;
            padding-bottom: 20px;

            .row {
                div {

                    &:not(:last-of-type) {
                        margin-bottom: 50px;
                    }

                    .social_link {
                        @include menu-social-media;
                        margin-top: 25px;
                    }

                    ul {
                        li {
                            a {
                                img {
                                    max-width: 100px;
                                    margin-top: 20px;
                                    margin-right: 20px;
                                }
                            }
                        }
                    }
                }
            }
        }
    }
</style>