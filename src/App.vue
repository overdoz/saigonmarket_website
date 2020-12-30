<template>
    <div id="app">
        <Header/>
        <OpnHours/>
        <Food/>
        <About/>
        <Footer/>
    </div>

</template>

<script>
    import Header from "./sections/Header.vue";
    import OpnHours from "./sections/OpnHours.vue";
    import Food from "./sections/Food.vue";
    import About from "./sections/About.vue";
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
    p, h1, h2, h3, h4, a, li {
        font-family: 'Stylish', sans-serif;
        text-decoration: none;
    }

    #app {
        height: 100%;
        width: 100%;
        margin: 0;
        padding: 0;
    }

    .fade-enter-active, .fade-leave-active {
        transition: opacity .5s;
    }
    .fade-enter, .fade-leave-to /* .fade-leave-active below version 2.1.8 */ {
        opacity: 0;
    }

    .bounce-enter-active {
        animation: bounce-in 1.5s;
    }
    .bounce-leave-active {
        animation: bounce-in 1.5s reverse;
    }
    @keyframes bounce-in {
        0% {
            transform: scale(0);
        }
        50% {
            transform: scale(1.25);
        }
        100% {
            transform: scale(1);
        }
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

    @-moz-keyframes slide {
        100% { -moz-transform: translateX(1vw); }
    }
    @-webkit-keyframes slide {
        100% { -webkit-transform: translateX(1vw); }
    }
    @keyframes slide {
        100% { -webkit-transform: translateX(1vw); transform:translateX(1vw); }
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
