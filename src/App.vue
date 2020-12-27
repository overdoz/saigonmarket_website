<template>
    <div id="app">
        <Header/>
        <OpnHours/>
        <Food/>
        <About/>
        <Payment/>
        <Footer/>
    </div>

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
    p, h1, h2, h3, a {
        font-family: 'Stylish', sans-serif;
    }

    #app {
        height: 100%;
        width: 100%;
        margin: 0;
        padding: 0;
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

    @-moz-keyframes jump {
        100% { -moz-transform: translateY(1vh); }
    }
    @-webkit-keyframes jump {
        100% { -webkit-transform: translateY(1vh); }
    }
    @keyframes jump {
        100% { -webkit-transform: translateY(1vh); transform:translateY(1vh); }
    }

    @-moz-keyframes swing { 100% { -moz-transform: rotate(10deg); } }
    @-webkit-keyframes swing { 100% { -webkit-transform: rotate(10deg); } }
    @keyframes swing { 100% { -webkit-transform: rotate(10deg); transform:rotate(10deg); } }
</style>
