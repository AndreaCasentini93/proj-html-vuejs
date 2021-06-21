<template>
    <nav>
        <div class="d-flex justify-content-between align-items-center container">
            <a href="#">
                <img src="../assets/images/dark-logo.png" alt="Logo MaxCoach">
            </a>
            <ul class="d-flex align-items-center">
                <li v-for="n in 6" :key="n">
                    <a href="#">Link</a>
                </li>
            </ul>
            <ul class="d-flex align-items-center">
                <li v-for="n in 4" :key="n">
                    <a href="#">Social</a>
                </li>
            </ul>
        </div>
    </nav>
</template>

<script>
export default {
    name: 'Menu'
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
                li {
                    margin: 0 10px;
                }
            }
        }
    }

</style>