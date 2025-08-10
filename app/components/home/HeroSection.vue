<template>
    <section class="relative">
        <Swiper
            :modules="[Autoplay, Pagination]"
            :autoplay="{ delay: 4000, disableOnInteraction: false }"
            :pagination="{ clickable: true }"
            loop
            class="w-full h-[50vh] sm:h-[100vh]"
        >
            <SwiperSlide v-for="(slide, index) in slides" :key="index">
                <div
                    class="w-full h-full bg-cover bg-center"
                    :style="{ backgroundImage: `url(${slide})` }"
                ></div>
            </SwiperSlide>
        </Swiper>
    </section>
</template>


<script setup>
import { Swiper, SwiperSlide } from "swiper/vue";
import { Autoplay, Pagination } from "swiper/modules";

// Import CSS của Swiper
import "swiper/css";
import "swiper/css/pagination";

const slides = ["images/hero_1.png", "images/hero_2.png"];
</script>

<style scoped>
/* Tùy chỉnh chấm tròn pagination */
.swiper-pagination-bullet {
    background-color: white;
    opacity: 0.7;
}
.swiper-pagination-bullet-active {
    background-color: #b4995a; /* màu vàng giống header */
    opacity: 1;
}
</style>
