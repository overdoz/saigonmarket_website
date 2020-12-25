<template>
    <div class="app">
        <Header/>
        <OpnHours/>
        <Food/>
    </div>
<!--  <img alt="Vue logo" src="./assets/logo.png" />-->
<!--  <HelloWorld msg="Hello Vue 3.0 + Vite" />-->
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import Header from "./components/Header.vue";
import OpnHours from "./components/OpnHours.vue";
import Food from "./components/Food.vue";

export default {
  name: 'App',
  components: {
      Food,
      OpnHours,
    Header,
    HelloWorld
  }
}
</script>

<style>
    @font-face {
        font-family: "Pigae";
        src: local("Pigae"),
        url(./fonts/Pigae.ttf) format("truetype");
    }
    * {
        margin: 0 !important;
        overflow-x: hidden;
    }
  body {
    background-color: #98BEB6;
    padding: 0;
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

</style>
