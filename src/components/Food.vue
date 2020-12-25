<template>
    <div class="food">
        <svg class="food__blob" viewBox="0 0 200 200" xmlns="http://www.w3.org/2000/svg">
            <path fill="#FDC831" d="M42.3,-61.4C50.5,-52.4,49.7,-34.1,55.6,-17.6C61.6,-1.2,74.3,13.5,73.1,25.9C72,38.2,57.1,48.1,42.6,58.3C28.1,68.5,14,79,-2.1,81.9C-18.2,84.7,-36.4,79.9,-45.2,67.9C-53.9,55.8,-53.3,36.4,-52.9,21.1C-52.5,5.7,-52.4,-5.6,-49.5,-16.6C-46.7,-27.6,-41,-38.1,-32.3,-47C-23.6,-55.9,-11.8,-63,2.7,-66.6C17.1,-70.3,34.2,-70.4,42.3,-61.4Z" transform="translate(100 100)" />
        </svg>
        <h2>
            Speisekarte
        </h2>
        <div class="food__page">
            <div class="food__page">
                <h3>Nudelgerichte</h3>
            </div>
        </div>
    </div>
</template>

<script>
    export default {
        name: "Food"
    }
</script>

<style scoped>
    h2 {
        padding: 20px;
    }
    .food {
        position: relative;
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        overflow-y: scroll !important;

    }
    .food__blob {
        position: absolute;
        left: -30vw;
        top: -5vw;
        height: 60vw;
        width: 80vw;
        z-index: 0;
 }
    .food__page {
        height: 135vw;
        width: 90vw;
        background-color: white;
        z-index: 2;
    }
</style>