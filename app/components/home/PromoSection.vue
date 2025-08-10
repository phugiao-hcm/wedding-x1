<template>
    <section class="bg-[#f7f1e8] py-8">
        <div class="max-w-10xl mx-auto">
            <!-- Tiêu đề -->
            <h2 class="text-center text-3xl font-bold text-[#5a3e1b] mb-6">
                TRI ÂN
                <span class="italic font-normal text-[#b4995a]"
                    >Khách hàng</span
                >
            </h2>

            <!-- Swiper -->
            <Swiper
                :slides-per-view="1"
                :space-between="16"
                :loop="true"
                :autoplay="{ delay: 3000, disableOnInteraction: false }"
                :breakpoints="{
                    640: { slidesPerView: 1 },
                    768: { slidesPerView: 2 },
                    1024: { slidesPerView: 3 },
                }"
                class="promo-swiper"
            >
                <SwiperSlide v-for="(item, index) in promos" :key="index">
                    <img
                        :src="item"
                        alt="Khuyến mãi"
                        class="w-full h-auto object-cover rounded-lg"
                    />
                </SwiperSlide>
            </Swiper>
        </div>
    </section>
</template>

<script setup>
import { Swiper, SwiperSlide } from "swiper/vue";
import "swiper/css";
import "swiper/css/autoplay";

const promos = [
    "images/trian_1.png",
    "images/trian_2.png",
    "images/trian_3.png",
    "images/trian_1.png",
    "images/trian_2.png",
    "images/trian_3.png",
];
</script>

<style scoped>
.promo-swiper {
    padding-bottom: 20px;
}
</style>
