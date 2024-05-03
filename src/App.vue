<script>
    import AppHeader from './components/AppHeader.vue';
    import AppMain from './components/AppMain.vue';
    import AppIcons from './components/AppIcons.vue';
    import AppFooter from './components/AppFooter.vue';

    export default {
        components: {
            AppHeader,
            AppMain,
            AppIcons,
            AppFooter
        }
    }

</script>

<template>
    <div class="container">
        <AppHeader />
        <AppMain />
        <AppIcons />
        <AppFooter />
    </div>

</template>

<style lang="scss">

</style>