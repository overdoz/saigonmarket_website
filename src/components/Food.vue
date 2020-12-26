<template>
    <div class="food">
        <svg class="food__blob" viewBox="0 0 200 200" xmlns="http://www.w3.org/2000/svg">
            <path fill="#FDC831"
                  d="M42.3,-61.4C50.5,-52.4,49.7,-34.1,55.6,-17.6C61.6,-1.2,74.3,13.5,73.1,25.9C72,38.2,57.1,48.1,42.6,58.3C28.1,68.5,14,79,-2.1,81.9C-18.2,84.7,-36.4,79.9,-45.2,67.9C-53.9,55.8,-53.3,36.4,-52.9,21.1C-52.5,5.7,-52.4,-5.6,-49.5,-16.6C-46.7,-27.6,-41,-38.1,-32.3,-47C-23.6,-55.9,-11.8,-63,2.7,-66.6C17.1,-70.3,34.2,-70.4,42.3,-61.4Z"
                  transform="translate(100 100)"/>
        </svg>
        <div class="food__titlebar">
            <img class="chopstick" src="../assets/chopstick.svg">

            <h2>
                Speisekarte
            </h2>
        </div>
        <div class="food__slider">
            <VueScrollSnap :horizontal="true">
                <section class="food__page">
                    <div class="food__sheet">
                        <h3>Nudelgerichte</h3>
                        <div class="food__dish" v-for="item in food.Suppen">
                            <div class="food__page-row first-line">
                                <div class="food__page-row">
                                    <p class="food__id">{{item.id}}</p>
                                    <p class="bold">{{item.name}}</p>
                                </div>
                                <p class="bold">{{item.price}} €</p>
                            </div>
                            <p>{{item.desc}}</p>
                        </div>
                    </div>
                </section>

                <section class="food__page">
                    <div class="food__sheet">
                        <h3>Nudelgerichte</h3>
                    </div>
                </section>
                <section class="food__page">
                    <div class="food__sheet">
                        <h3>Nudelgerichte</h3>
                    </div>
                </section>
            </VueScrollSnap>

        </div>
    </div>
</template>

<script>
    import VueScrollSnap from "vue-scroll-snap";

    export default {
        name: "Food",
        components: {VueScrollSnap},
        data() {
            return {
                food: {
                    Suppen: [
                        {id: "01", name: "Mien Ga", price: 6.0, desc: "Klare Hühnerbrühe mit Glasnudeln und Hühnerfilet"},
                        {id: "02", name: "Wantan Suppe (G)", price: 4.5, desc: "Teigtaschen gefüllt mit Schweinefleisch und Garnelen, Hühnerbrühe, Sojasprossen"},
                        {id: "03", name: "Udon Nudeln Suppe (F)", price: 6.0, desc: "Udon Nudeln mit Garnelen & Schweinefleisch Mix in Gemüsebrühe"},
                        {id: "04", name: "Pho (F)", price: 8.0, desc: "Kräftig klare Rinderbrühe mit Reisnudeln, Rindfleisch, frische Kräuter, Sternanis, Kardamon, Zwiebeln"},
                    ]
                }
            }
        },
    }
</script>

<style scoped>
    h2 {
        padding: 10px;
        font-size: 8vw;
        color: #645585;

    }
    h3 {
        margin: 0;
        color: #E30615;
    }
    p {
        margin: 0;
    }
    .bold {
        font-weight: bold;
    }
    .chopstick {
        height: 40vw;
        width: auto;
        transform: rotate(30deg);
        margin-right: 5vw;
        margin-left: 15vw;
    }

    .food__page-row {
        display: flex;
        flex-direction: row;
    }

    .food__dish {
        margin: 12px 8px;
    }

    .food__id {
        font-weight: bold;
        margin-right: 1rem;
        color: #E30615;
    }

    .first-line {
        justify-content: space-between;
    }

    .food {
        padding-bottom: 10px;
        position: relative;
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        overflow-y: visible !important;
        z-index: 0;
        scroll-snap-type: x mandatory;
        scroll-padding: 50%;

    }

    .food__blob {
        position: absolute;
        left: -30vw;
        top: -10vw;
        height: 60vw;
        width: 100vw;
        z-index: -1;
        overflow-y: visible !important;

    }

    .food__titlebar {
        width: 100%;
        display: flex;
        flex-direction: row;
        align-items: center;
        justify-content: space-evenly;
    }

    .food__slider {
        scroll-snap-type: x mandatory;
        width: 100vw;
        scroll-padding: 50%;
    }

    .food__page {
        height: 135vw;
        width: 100vw;
        padding: 4vw;
        z-index: 2;
        scroll-snap-align: start;

    }

    .food__sheet {
        background-color: white;
        box-shadow: 2px 2px 5px black;
        width: 80vw;
        height: 70vh;
        padding: 10px;
        display: flex;
        flex-direction: column;

    }
</style>