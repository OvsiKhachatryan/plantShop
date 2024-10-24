<script setup>
import Navbar from "./components/Navbar.vue";
import Banner from "./components/Banner.vue";
import Deal from "./components/Deal.vue";
import Shop from "./components/Shop.vue";
import PlantCollection from "./components/PlantCollection.vue";
import CustomersSay from "./components/CustomersSay.vue";
import Footer from "./components/Footer.vue";
</script>

<template>
    <div class="plant-collection-list">
        <div class="plant-first"></div>
        <div class="plant-second"></div>
        <div class="plant-third"></div>
    </div>
    <Navbar/>
    <Banner/>
    <Deal/>
    <Shop />
    <PlantCollection />
    <CustomersSay />
    <Footer />
</template>

<style scoped>
.plant-first,
.plant-second,
.plant-third {
    position: absolute;
    background-size: cover;
    background-repeat: no-repeat;
}

/* Styles for the first plant */
.plant-first {
    width: 80px;
    height: 600px;
    background-image: url("/assets/images/plant/plant-1.png");
}

/* Styles for the second plant */
.plant-second {
    width: 207px;
    height: 218px;
    top: 550px; /* Adjust as needed */
    background-image: url("/assets/images/plant/plant-2.png");
}

/* Styles for the third plant */
.plant-third {
    right: 0;
    top: -55px; /* Adjust as needed */
    width: 74px;
    height: 391px;
    background-image: url("/assets/images/plant/plant-3.png");
}

</style>
