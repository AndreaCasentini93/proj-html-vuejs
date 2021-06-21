<template>
    <div id="countdown" class="d-flex justify-content-center align-items-center">
        <div>Starts TOMORROW! Our biggest event of the year...</div>
        <div>
            <i class="far fa-clock"></i>
            <span>00 : 00 : 00 : 00</span>
        </div>
        <div>
            <a href="#">Get ticket</a>
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
        background-color: $bg-color;

        div {
            padding: 10px 15px;

            i {
                margin-right: 10px;
            }
        }
    }
</style>