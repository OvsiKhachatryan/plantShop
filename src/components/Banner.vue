<script setup>
import {ref, computed, onMounted, onBeforeUnmount} from 'vue';

const slides = ref([
    {id: 1, image: '/assets/images/plant/plant-4.png'},
    {id: 2, image: '/assets/images/plant/plant-7.png'},
    {id: 3, image: '/assets/images/plant/plant-4.png'},
    {id: 4, image: '/assets/images/plant/plant-7.png'}
]);

const activeIndex = ref(0);

const totalSlides = computed(() => slides.value.length);
const updateCounter = (event) => {
    activeIndex.value = event.to;
};

let carouselInstance = null;
onMounted(() => {
    const carouselElement = document.getElementById('carouselExample');
    carouselInstance = new bootstrap.Carousel(carouselElement);

    carouselElement.addEventListener('slide.bs.carousel', updateCounter);
});

onBeforeUnmount(() => {
    if (carouselInstance) {
        const carouselElement = document.getElementById('carouselExample');
        carouselElement.removeEventListener('slide.bs.carousel', updateCounter);
        carouselInstance.dispose();
    }
});
</script>

<template>
    <div
            id="carouselExample"
            class="carousel slide"
            data-bs-ride="carousel"
            @slide.bs.carousel="updateCounter"
    >
        <div class="carousel-inner">
            <div
                    v-for="(slide, index) in slides"
                    :key="slide.id"
                    :class="['carousel-item', { active: index === activeIndex }]"
            >
                <div class="section-banner col-lg-12 d-flex flex-wrap wrap justify-content-between align-items-center">
                    <div class="content col-lg-4">
                        <h3 class="subheading">Let’s Bring</h3>
                        <h1 class="heading">A New Friend Home</h1>
                        <div class="about">
                            Lorem ipsum dolor sit amet, consectetur adipiscing elit. Proin dapibus
                            diam in consequat tempor. Donec eget justo ut est pretium gravida.
                            Phasellus vulputate erat ipsum, nec gravida magna sodales in.
                        </div>
                        <div class="d-flex align-items-center mt-4 section-price">
                            <button class="btn btn-shop me-4">Shop Now</button>
                            <div>New Price: <span class="price">$ 30</span></div>
                        </div>
                    </div>
                    <div class="section-image col-lg-5">
                        <div class="image d-flex justify-content-center align-items-center">
                            <img :src="slide.image" alt="plant"/>
                        </div>
                        <div class="banner-count mt-5 d-flex justify-content-center align-items-center">
                            <div class="line me-3"></div>
                            <div>
                                <p class="slide-step">0{{ activeIndex + 1 }}/<span class="slide-count">0{{
                                    totalSlides
                                    }}</span></p>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<style scoped>
.section-banner {
    width: 1279px;
    margin: 166px auto 0 auto;
    padding: 0 10px 0 120px;
}

.section-banner .content {
    width: 620px;
    height: 280px;
    margin-top: -102px;
}

.content .subheading, .heading {
    color: var(--main-color);
    font-weight: bold;
}

.content .heading {
    font-size: 69px;
}

.about {
    max-width: 511px;
    min-height: 100px;
    font-size: 18px;
    padding-right: 22px;
}

.btn-shop {
    background-color: var(--main-color);
    color: var(--white);
}

.image {
    position: relative;
    width: 450px;
    height: 490px;
    background-color: var(--plant-bg-color);
    border-radius: 50% 50% 0 0;
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1),
    0 6px 20px rgba(0, 0, 0, 0.1);
}

.image img {
    position: absolute;
    top: -75px;
}

.price {
    color: var(--main-color);
}

.banner-count {
    width: 177px;
    height: 30px;
}

.banner-count .line {
    width: 108px;
    height: 10px;
    border-top: 1px solid gray;
    border-left: none;
    border-right: none;
    border-bottom: none;
}

.slide-step {
    font-size: 25px;
    font-weight: bold;
    color: var(--main-color);
}

.slide-count {
    font-size: 14px;
    font-weight: normal;
    color: var(--main-color);
}

.section-banner {
    position: relative;
}

.carousel-inner {
    width: 100%;
}

.banner-count {
    font-size: 18px;
    text-align: center;
}

/* Extra Small Devices */
@media (max-width: 575px) {
    .section-banner {
        margin: 40% 0 0 0;
        padding: 35px;
        flex-wrap: wrap;
        width: 100%;
        justify-content: center !important;
    }

    .subheading {
        font-size: 15px;
    }

    .heading {
        font-size: 25px !important;
    }

    .section-price {
        display: flex;
        flex-direction: column;
    }

    .btn-shop {
        width: 100% !important;
    }

    .about {
        text-align: justify;
        font-size: 13px;
    }

    .image {
        height: 300px;
        width: 100%;
        margin-top: 100px;
    }

    .image img {
    //width: 100%; top: -14px; height: 100%;
    }

}

/* Small Devices */
@media (min-width: 576px) and (max-width: 767px) {
    .section-banner {
        margin: 40% 0 0 0;
        padding: 35px;
        flex-wrap: wrap;
        width: 100%;
        justify-content: center !important;
    }

    .subheading {
        font-size: 15px;
    }

    .heading {
        font-size: 30px !important;
    }

    .section-price {
        display: flex;
        flex-direction: column;
    }

    .btn-shop {
        width: 100% !important;
    }

    .about {
        text-align: justify;
        font-size: 15px;
    }

    .image {
        height: 300px;
        width: 100%;
        margin-top: 100px;
    }

    .image img {
    //width: 100%; top: -14px; height: 100%;
    }

}

/* Medium Devices */
@media (min-width: 768px) and (max-width: 991px) {
    .section-banner {
        padding: 50px 50px 0 120px;
        width: 100%;
        justify-content: center !important;
    }

    .heading {
        font-size: 50px;
    }

    .subheading {
        font-size: 20px;
    }

    .about {
        font-size: 14px;
    }

    .section-image {
        margin-top: 100px;
    }
}

/* Large Devices */
@media (min-width: 992px) and (max-width: 1199px) {
    .section-banner {
        justify-content: center !important;
    }

    #carouselExample {
        width: 100%;
    }

    .heading {
        font-size: 55px !important;
    }

    .image {
        width: 300px;
        height: 376px;
    }

    .image img {
        height: 100% !important;
        top: -22px;
    }

    .content{
        width: 600px;
    }
}

/* Extra Large Devices */
@media (min-width: 1200px) {
    /* Styles for extra large devices */
}
</style>