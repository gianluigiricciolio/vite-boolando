<script>
import HeaderApp from './components/HeaderApp.vue';
import MainApp from './components/MainApp.vue';
import FooterApp from './components/FooterApp.vue';

export default {
    components: {
        HeaderApp,
        FooterApp,
        MainApp,
    }

}

</script>

<template>
    <header>
        <HeaderApp></HeaderApp>
    </header>

    <main>
        <MainApp></MainApp>
    </main>

    <footer>
        <FooterApp></FooterApp>
    </footer>
</template>
