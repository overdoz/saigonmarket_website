<template>
    <div class="app">
        <Header/>
        <OpnHours/>
        <Food/>
        <About/>
        <Payment/>
        <Footer/>
    </div>
<!--      <img alt="Vue logo" src="./assets/logo.png" />-->
<!--      <HelloWorld msg="Hello Vue 3.0 + Vite" />-->
</template>

<script>
    import Header from "./components/Header.vue";
    import OpnHours from "./components/OpnHours.vue";
    import Food from "./components/Food.vue";
    import About from "./components/About.vue";
    import Payment from "./sections/Payment.vue";
    import Footer from "./sections/Footer.vue";

    export default {
        name: 'App',
        components: {
            Footer,
            Payment,
            About,
            Food,
            OpnHours,
            Header,
        }
    }
</script>

<style>
    @font-face {
        font-family: "Pigae";
        src: local("Pigae"),
        url(./fonts/Pigae.ttf) format("truetype");
    }

    html, body {
        margin: 0 !important;
        overflow-x: hidden;
    }

    body {
        background-color: #98BEB6;
        padding: 0;
    }
    p, h1, h2, h3 {
        font-family: 'Stylish', sans-serif;
    }

    #app {
        height: 100%;
        width: 100%;
        margin: 0;
        padding: 0;
    }

    .app {
        height: 100%;
        width: 100%;

    }

    @-moz-keyframes spin360 {
        100% { -moz-transform: rotate(360deg); }
    }
    @-webkit-keyframes spin360 {
        100% { -webkit-transform: rotate(360deg); }
    }
    @keyframes spin360 {
        100% { -webkit-transform: rotate(360deg); transform:rotate(360deg); }
    }
    @keyframes fadeIn {
        0% {opacity:0; transform: translateX(20vw)}
        100% {opacity:1; transform: translateX(0)}
    }

    @-moz-keyframes fadeIn {
        0% {opacity:0;}
        100% {opacity:1;}
    }

    @-webkit-keyframes fadeIn {
        0% {opacity:0;}
        100% {opacity:1;}
    }
</style>
