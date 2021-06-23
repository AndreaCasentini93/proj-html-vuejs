<template>
    <div class="position-relative single_card">
        <img :src="card.image" :alt="card.title">
        <div class="wrapper">
            <h5>{{ card.subTitle }}</h5>
            <h4>{{ card.title }}</h4>
            <div class="d-flex align-items-center icon_box">
                <i :class="card.classIcon1"></i><span>{{ card.textIcon1 }}</span>
                <i :class="card.classIcon2"></i><span>{{ card.textIcon2 }}</span>
            </div>
        </div>
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

    // COMMONS
    .single_card{
        .wrapper{
            position: relative;
            width: 100%;
            height: 100%;
        }
    }

    // COURSES CARDS
    .courses_cards {

        .single_card {
            padding: 35px 20px;

            img {
                max-width: 100%;
                margin-bottom: 20px;
            }

            h5 {
                font-size: 15px;
                font-weight: 700;
                color: $ashtag-color;
            }

            h4 {
                width: 70%;
                margin-bottom: 20px;
                font-size: 16px;
                font-weight: 700;
                color: $sub-title-color;
            }

            .icon_box {
                font-size: 12px;
                vertical-align: middle;
                color: $base-color;

                i {
                    margin-right: 5px;
                    font-size: 13px;
                }

                span {
                    margin-right: 10px;
                }
            }
        }

    }

    // ARTICLES CARDS
    .articles_cards {
        
        .single_card {
            margin: 0 20px;
            background-color: #FFFFFF;
            box-shadow: 0 0 20px 1px lighten($base-color, 40%);

            img {
                max-width: 100%;
            }

            &:first-of-type,
            &:last-of-type {
                width: 250px;

                .wrapper {
                    padding: 10px;
                }

                img {
                    margin: 0;
                    margin-bottom: 20px;
                }

                h5 {
                    text-transform: uppercase;
                    font-size: 13px;
                    font-weight: 600;
                    color: $base-color;
                }

                h4 {
                    margin-bottom: 10px;
                    font-size: 18px;
                    font-weight: 700;
                    color: $sub-title-color;
                }

                .icon_box {
                    font-size: 12px;
                    vertical-align: middle;
                    color: $base-color;

                    i {
                        margin-right: 5px;
                        font-size: 12px;
                    }

                    span {
                        margin-right: 25px;
                    }
                }
            }

            &:first-of-type {
                align-self: center;
                margin-top: 40px;
                margin-bottom: 40px;
            }
            &:last-of-type {
                align-self: flex-start;
                margin-top: 40px;
            }

            &:nth-of-type(2) {
                align-self: center;
                color: #FFFFFF;

                .wrapper {
                    display: flex;
                    flex-direction: column;
                    justify-content: flex-end;
                    position: absolute;
                    top: 0;
                    left: 0;
                    padding: 40px 20px;
                    background-color: $bg-opaque;
                }

                img {
                    display: block;
                    width: 100%;
                }

                h5 {
                    text-transform: uppercase;
                    font-size: 15px;
                    margin-bottom: 8px;
                }

                h4 {
                    line-height: 1.5;
                    margin-bottom: 8px;
                    font-size: 35px;
                    font-weight: 700;
                }

                .icon_box {
                    font-size: 14px;
                    vertical-align: middle;

                    i {
                        margin-right: 5px;
                        font-size: 14px;
                    }

                    span {
                        margin-right: 25px;
                    }
                }
            }
        }
    }

    @media screen and (max-width: 767px) {

        .single_card:nth-of-type(2) {
            h5 {
                font-size: 13px !important;
            }

            h4 {
                font-size: 18px !important;
            }

            .icon_box {
                font-size: 12px !important;

                i {
                    font-size: 12px !important;
                }
            }
        }

    }

</style>