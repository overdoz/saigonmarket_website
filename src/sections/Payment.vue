<template>
    <div class="payment">
        <img src="../assets/american-express.png">
        <img src="../assets/applepay.png">
        <img src="../assets/ec.png">
        <img src="../assets/googlepay.png">
        <img src="../assets/mastercard.png">
        <img src="../assets/maestro.png">
        <img src="../assets/visa-alternate.png">
    </div>
</template>

<script>
    export default {
        name: "Payment"
    }
</script>

<style scoped>
    .payment {
        background-color: white;
        display: flex;
        justify-content: center;
        align-items: center;
    }
    img {
        width: 10vw;
        height: auto;
        margin: 8px;
    }
</style>