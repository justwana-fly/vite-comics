<template>
    <HeaderComponent />
    <MainComponent />
    <FooterComponent />


</template>

<script>
    import HeaderComponent from './components/HeaderComponent.vue';
    import MainComponent from './components/MainComponent.vue';
    import FooterComponent from './components/Footer.component.vue';
    export default {
        name: 'App',
        components: {
            HeaderComponent,
            MainComponent,
            FooterComponent
        }
    }
</script>

<style lang="scss" scoped>

h2 {
    color: red;
}
</style>