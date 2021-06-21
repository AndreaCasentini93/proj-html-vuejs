<template>
    <div id="countdown" class="d-flex justify-content-center align-items-center">
        <div>Starts TOMORROW! Our biggest event of the year...</div>
        <div class="countdown-time">
            <i class="far fa-clock"></i>
            <span>00 : 00 : 00 : 00</span>
        </div>
        <div>
            <a href="#" class="btn_type_1">Get ticket</a>
        </div>
    </div>
</template>

<script>
export default {
    name: 'Countdown'
}
</script>

<style lang="scss" scoped>
    @import '../assets/style/variables.scss';
    @import '../assets/style/mixins.scss';

    #countdown {
        background-color: $bg-countdown;

        div {
            margin: 13px 15px;
            font-size: 12px;
            color: $base-color;
        }

        .countdown-time {
            font-size: 14px;
            font-weight: 700;
            color: $logo-color;
            
            i {
                margin-right: 10px;
            }
        }
    }
</style>