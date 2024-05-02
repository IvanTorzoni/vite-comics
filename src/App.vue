<script>
    import AppHeader from './components/AppHeader.vue';
    import AppMain from './components/AppMain.vue';
    import AppFooter from './components/AppFooter.vue';

    export default {
        components: {
            AppHeader,
            AppMain,
            AppFooter
        }
    }

</script>

<template>
    <div class="container">
        <AppHeader />
        <AppMain />
        <AppFooter />
    </div>

</template>

<style lang="scss">

.container {
    display: flex;
    flex-direction: column;
    width: 80%;
    margin: 0 auto;
}
</style>