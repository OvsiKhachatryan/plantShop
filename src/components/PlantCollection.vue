<script setup>

</script>

<template>
    <h4 class="collection-title text-center">Plant Collection</h4>
    <div class="d-flex justify-content-center align-items-center mt-4 plants-block">
        <div class="item-first d-flex justify-content-center align-items-center me-3">
            <div class="section-shop">
                <h3 class="text-center text-white">Indoor Plants</h3>
                <div class="d-flex justify-content-center">
                    <button class="btn btn-shop-now">Shop Now</button>
                </div>
            </div>
            <img src="/assets/images/plant/indoor.avif" alt="plant">
        </div>
        <div class="item-second d-flex justify-content-center align-items-center">
            <div class="section-shop">
                <h3 class="text-center text-white">Outdoor Plants</h3>
                <div class="d-flex justify-content-center">
                    <button class="btn btn-shop-now">Shop Now</button>
                </div>
            </div>
            <img src="/assets/images/plant/outdoor.jpg" alt="plant">
        </div>
    </div>
</template>

<style scoped>
.collection-title {
    color: var(--main-color)
}

.item-first, .item-second {
    width: 620px;
    height: 424px;
    background-size: cover;
    background-repeat: no-repeat;
    background-position: center;
    position: relative;
}

.item-first img {
    object-fit: cover;
    width: 100%;
    height: 100%;
}

.item-second img {
    object-fit: cover;
    width: 100%;
    height: 100%;
}

.btn-shop-now {
    color: var(--main-color);
    background-color: var(--white);
}

.section-shop {
    position: absolute;
}

/* Extra Small Devices */
@media (max-width: 575px) {
    .plants-block{
        flex-direction: column;
    }

    .item-second{
        margin-top: 10px;
    }

    .item-first, .item-second{
        width: 100%;
    }
}

</style>