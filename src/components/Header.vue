<template>
    <div class="header">
        <svg class="header__blob" viewBox="0 0 200 200" xmlns="http://www.w3.org/2000/svg">
            <path fill="#FDC831"
                  d="M28,-38.8C36.2,-32.7,42.7,-24.3,47.6,-14.3C52.5,-4.2,56,7.6,53.9,18.6C51.7,29.6,44.1,39.8,34.2,48.1C24.3,56.4,12.1,62.8,0.7,61.8C-10.7,60.8,-21.4,52.6,-32,44.5C-42.6,36.4,-53,28.5,-60.6,16.9C-68.1,5.4,-72.8,-9.9,-68.2,-21.5C-63.5,-33.1,-49.5,-41,-36.6,-45.6C-23.7,-50.2,-11.9,-51.4,-1,-50.1C9.9,-48.8,19.9,-44.9,28,-38.8Z"
                  transform="translate(100 100)"/>
        </svg>
        <svg class="header__title" xmlns="http://www.w3.org/2000/svg" width="176" height="45" viewBox="0 0 176 45">
            <g id="Gruppe_20" data-name="Gruppe 20" transform="translate(-178 -233)">
                <text id="Sai_Gon_Market" data-name="Sai Gon Market" transform="translate(268 265)" fill="#e30615"
                      font-size="30" font-family="Pigae">
                    <tspan x="-85.29" y="0">Sai Gon Market</tspan>
                </text>
                <text id="Sai_Gon_Market-2" data-name="Sai Gon Market" transform="translate(267 264)" fill="#fff"
                      font-size="30" font-family="Pigae">
                    <tspan x="-85.29" y="0">Sai Gon Market</tspan>
                </text>
            </g>
        </svg>
        <img class="header__logo" src="../assets/logo.svg">


    </div>

</template>

<script>
    export default {
        name: "Header"
    }
</script>

<style scoped>
    * {
        overflow-x: hidden;
    }

    .header__blob {
        height: 120vw;
        width: 160vw;
        position: absolute;
        right: -40vw;
        top: -50vw;
        -webkit-animation:spin360 60s linear infinite;
        -moz-animation:spin360 60s linear infinite;
        animation:spin360 60s linear infinite;

    }

    .header__title {
        height: 15vw;
        width: auto;
        position: absolute;
        right: 0;
        top: 65vw;
        margin: 20px;
        animation: fadeIn ease 1s;
        -webkit-animation: fadeIn ease 1s;

    }

    .header__logo {
        position: absolute;
        z-index: 2;
        width: 85vw;
        height: auto;
        left: -30vw;
        top: -10vw;
        animation: fadeIn ease 5s;
        -webkit-animation: fadeIn ease 5s;

    }

    .header {
        position: relative;
        width: 100vw;
        height: 90vw;
        overflow: hidden;
    }
</style>