<template>
    <div class="footer">
        <svg class="blob" viewBox="0 0 200 200" xmlns="http://www.w3.org/2000/svg">
            <path fill="#FDC831" d="M39.9,-67.5C51.5,-62.3,60.7,-51.3,69.8,-39.1C78.9,-26.9,87.9,-13.5,85.1,-1.6C82.4,10.3,68,20.6,59.1,33C50.1,45.5,46.5,59.9,37.6,63.8C28.6,67.7,14.3,60.9,-1.1,62.8C-16.5,64.6,-32.9,75.1,-43.8,72.4C-54.8,69.6,-60.2,53.8,-62.9,39.5C-65.6,25.2,-65.5,12.6,-68,-1.5C-70.6,-15.5,-75.7,-31.1,-72.7,-44.8C-69.7,-58.5,-58.6,-70.4,-45.1,-74.6C-31.7,-78.8,-15.8,-75.4,-0.9,-73.9C14.1,-72.3,28.2,-72.8,39.9,-67.5Z" transform="translate(100 100)" />
        </svg>
        <div class="footer__links">
            <h3>
                Rechtliches
            </h3>
            <a>Impressum</a>
        </div>
    </div>
</template>

<script>
    export default {
        name: "Footer"
    }
</script>

<style scoped>
    .footer {
        position: relative;
        height: 50vw;
        overflow: hidden;
        color: #E30615;
    }
    .blob {
        position: absolute;
        height: 80vw;
        width: auto;
        left: -20vw;
        bottom: -30vw;
    }
    .footer__links {
        position: absolute;
        left:10px;
        bottom: 10px;
    }
</style>