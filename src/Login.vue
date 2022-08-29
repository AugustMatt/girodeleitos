<script setup>
    import LoadingScreen from './components/login/LoadingScreen.vue'
    import LoginHeader from './components/login/Header.vue';
    import LoginContent from './components/login/Content.vue';
    import LoginFooter from './components/login/Footer.vue';

</script>

<template>

    <LoadingScreen />

    <div class="login">
        <LoginHeader />
        <LoginContent />
        <LoginFooter />
    </div>

</template>

<style>
    @import '../node_modules/bootstrap/dist/css/bootstrap.css';

    .login {
        background-color: aqua;
        height: 100vh;
        z-index: 1;
    }

</style>
