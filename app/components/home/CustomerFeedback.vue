<template>
    <section class="py-16 bg-pink-50">
        <div class="max-w-6xl mx-auto px-4 text-center">
            <h2 class="text-3xl font-bold text-gray-800 mb-10">
                Khách hàng nói gì về chúng tôi
            </h2>

            <Swiper
                :modules="[Pagination, Autoplay]"
                :slides-per-view="1"
                :space-between="30"
                :autoplay="{ delay: 4000 }"
                :pagination="{ clickable: true }"
                loop
                class="pb-10"
            >
                <SwiperSlide
                    v-for="(feedback, index) in feedbacks"
                    :key="index"
                >
                    <div
                        class="bg-white p-8 rounded-2xl shadow-lg max-w-3xl mx-auto relative"
                    >
                        <svg
                            xmlns="http://www.w3.org/2000/svg"
                            class="w-10 h-10 text-pink-300 absolute -top-4 left-4"
                            fill="currentColor"
                            viewBox="0 0 24 24"
                        >
                            <path
                                d="M7.17 6A5.17 5.17 0 0 0 2 11.17V20h8v-8H6.83A3.17 3.17 0 0 1 10 8.83V6H7.17zm9 0A5.17 5.17 0 0 0 11 11.17V20h8v-8h-3.17A3.17 3.17 0 0 1 19 8.83V6h-2.83z"
                            />
                        </svg>
                        <p class="text-lg text-gray-600 italic mb-6">
                            "{{ feedback.comment }}"
                        </p>
                        <div class="flex items-center justify-center space-x-4">
                            <img
                                :src="feedback.image"
                                alt="avatar"
                                class="w-14 h-14 rounded-full border-2 border-pink-300"
                            />
                            <div class="text-left">
                                <h4 class="font-semibold text-gray-800">
                                    {{ feedback.name }}
                                </h4>
                                <p class="text-sm text-gray-500">
                                    {{ feedback.event }}
                                </p>
                            </div>
                        </div>
                    </div>
                </SwiperSlide>
            </Swiper>
        </div>
    </section>
</template>

<script setup>
import { Swiper, SwiperSlide } from "swiper/vue";
import { Pagination, Autoplay } from "swiper/modules";
import "swiper/css";
import "swiper/css/pagination";

const feedbacks = [
    {
        name: "Ngọc Anh & Minh Tuấn",
        event: "Tiệc cưới 2024",
        comment:
            "Nhà hàng trang trí rất đẹp, món ăn ngon và phục vụ tận tình. Gia đình và bạn bè đều rất hài lòng!",
        image: "https://randomuser.me/api/portraits/women/45.jpg",
    },
    {
        name: "Lan Hương",
        event: "Tiệc sinh nhật",
        comment:
            "Không gian rộng rãi, sang trọng và ấm cúng. Chắc chắn sẽ quay lại tổ chức sự kiện lần sau!",
        image: "https://randomuser.me/api/portraits/women/65.jpg",
    },
    {
        name: "Quốc Bảo",
        event: "Lễ kỷ niệm",
        comment:
            "Mọi thứ đều được chuẩn bị chu đáo, âm thanh ánh sáng chuyên nghiệp. Rất ấn tượng!",
        image: "https://randomuser.me/api/portraits/men/32.jpg",
    },
];
</script>

<style scoped>
.swiper-pagination-bullet {
    background-color: #ec4899; /* Màu hồng */
}
</style>
