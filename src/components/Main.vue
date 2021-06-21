<template>
    <main class="d-flex justify-content-center align-items-center">
        CONTENUTO DELLA PAGINA
    </main>
</template>

<script>
export default {
    name: 'Main'
}
</script>

<style lang="scss" scoped>
    @import '../assets/style/variables.scss';
    @import '../assets/style/mixins.scss';

    main {
        width: 100%;
        height: 150px;
        font-size: 30px;
        font-weight: 700;
        color: white;
        background-color: black;
    }
</style>