<template>
    <div class="modal">
        <div class="modal__sheet">
            <svg class="blob top" viewBox="0 0 200 200" xmlns="http://www.w3.org/2000/svg">
                <path fill="#FDC831"
                      d="M28,-38.8C36.2,-32.7,42.7,-24.3,47.6,-14.3C52.5,-4.2,56,7.6,53.9,18.6C51.7,29.6,44.1,39.8,34.2,48.1C24.3,56.4,12.1,62.8,0.7,61.8C-10.7,60.8,-21.4,52.6,-32,44.5C-42.6,36.4,-53,28.5,-60.6,16.9C-68.1,5.4,-72.8,-9.9,-68.2,-21.5C-63.5,-33.1,-49.5,-41,-36.6,-45.6C-23.7,-50.2,-11.9,-51.4,-1,-50.1C9.9,-48.8,19.9,-44.9,28,-38.8Z"
                      transform="translate(100 100)"/>
            </svg>
            <svg class="blob bottom" viewBox="0 0 200 200" xmlns="http://www.w3.org/2000/svg">
                <path fill="#FDC831"
                      d="M39.9,-67.5C51.5,-62.3,60.7,-51.3,69.8,-39.1C78.9,-26.9,87.9,-13.5,85.1,-1.6C82.4,10.3,68,20.6,59.1,33C50.1,45.5,46.5,59.9,37.6,63.8C28.6,67.7,14.3,60.9,-1.1,62.8C-16.5,64.6,-32.9,75.1,-43.8,72.4C-54.8,69.6,-60.2,53.8,-62.9,39.5C-65.6,25.2,-65.5,12.6,-68,-1.5C-70.6,-15.5,-75.7,-31.1,-72.7,-44.8C-69.7,-58.5,-58.6,-70.4,-45.1,-74.6C-31.7,-78.8,-15.8,-75.4,-0.9,-73.9C14.1,-72.3,28.2,-72.8,39.9,-67.5Z"
                      transform="translate(100 100)"/>
            </svg>
            <img class="close" src="../assets/cancel.svg" @click="$emit('close')"/>


            <div class="modal__titlerow modal__slot">
                <h2>{{ title }}</h2>
            </div>
            <div class="modal__slot">

            </div>
          <div class="modal__content">
            <slot>

            </slot>
          </div>


        </div>
    </div>
</template>

<script>
    export default {
        name: "Modal",
        props: {
            title: String,
        }
    }
</script>

<style scoped>
    h2, p {
        margin: 0;
        z-index: 100;
    }
    .blob {
        width: 90vw;
        height: auto;
        position: absolute;
        -webkit-animation: spin360 60s linear infinite;
        -moz-animation: spin360 60s linear infinite;
        animation: spin360 60s linear infinite;

    }

    .top {
        right: -35vw;
        top: -35vw;
    }

    .bottom {
        left: -15vw;
        bottom: -35vw;
    }

    .modal {
        display: flex;
        justify-content: center;
        align-items: center;
        width: 100vw;
        height: 100vh;
        position: fixed;
        z-index: 50;
        left: 0;
        top: 0;

    }
    .modal__slot {
        padding: 3vw;
        z-index: 100;
    }

    .modal__titlerow {
        width: 100%;
        display: flex;
        justify-content: center;
        align-items: center;

    }

    .modal__sheet {
        position: relative;
        width: 95vw;
        height: 60vh;
        background-color: #D1E9E4;
        box-shadow: 1px 1px 60vw black;
        overflow-y: scroll;
      overflow-x: hidden;

    }
    .modal__content {
      position: relative;
      overflow: scroll;
      z-index: 100;
    }

    .close {
        position: absolute;
        width: 5vw;
        height: auto;
        right: 5vw;
        top: 5vw;
    }
</style>
