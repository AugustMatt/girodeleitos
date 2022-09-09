<script setup>
    import LoadingScreen from './components/login/LoadingScreen.vue'
    import LoginHeader from './components/login/Header.vue';
    import LoginContent from './components/login/Content.vue';
    import LoginFooter from './components/login/Footer.vue';

</script>

<template>

    <LoadingScreen />

    <div class="w3layouts-main">
        <div class="bg-layer">
            <h1>Giro de Leitos - Login</h1>
            <div class="header-main">
                <LoginHeader />
                <LoginContent />
            </div>
            <LoginFooter />
        </div>
    </div>

</template>

<style>

@import url('./css/style.css');
@import url('./css/font-awesome.min.css');


html {
    overflow: hidden;
}
       
</style>
