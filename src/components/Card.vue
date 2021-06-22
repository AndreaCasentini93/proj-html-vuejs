<template>
    <div class="single_card">
        <img :src="card.image" :alt="card.title">
        <h5>&#xFF04;{{ card.subTitle }}</h5>
        <h4>{{ card.title }}</h4>
        <div class="d-flex align-items-center icon_box">
            <i :class="card.classIcon1"></i><span>{{ card.textIcon1 }}</span>
            <i :class="card.classIcon2"></i><span>{{ card.textIcon2 }}</span>
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

</style>