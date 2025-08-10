<template>
    <section>
        <!-- Phần mô tả -->
        <div
            class="bg-gradient-to-b from-[#f5e9d7] to-[#e3caa5] text-center px-6 py-12"
        >
            <h3 class="text-[#b4995a] italic text-2xl mb-2">Sự lựa chọn</h3>
            <h2 class="text-4xl font-bold text-[#5a3e1b] mb-6">ƯU VIỆT</h2>
            <p class="max-w-5xl mx-auto text-[#5a3e1b] leading-relaxed mb-4">
                Tọa lạc tại con đường sầm uất, Hương Phố hơn 20 năm qua đã được
                định vị là một trong những nhà hàng tiệc cưới lớn bởi Uy tín –
                Chất lượng – Kinh nghiệm – Giá cả. Khách hàng đến với Hương Phố
                luôn cảm thấy thoải mái và an tâm trước sự đa dạng của các món
                ăn, chất lượng dịch vụ do nhà hàng cung cấp. Sở hữu nhiều quy mô
                sảnh tiệc, chúng tôi hoàn toàn đáp ứng được lượng khách mời lớn
                nhỏ theo yêu cầu.
            </p>
            <p class="max-w-5xl mx-auto text-[#5a3e1b] leading-relaxed">
                Với 21 sảnh sang trọng và công suất lên tới 1000 khách mời tiệc,
                Hương Phố là lựa chọn xứng tầm cho những buổi tiệc cưới đầy dấu
                ấn. Được khách hàng đánh giá cao, Hương Phố đầu tư và đổi mới
                chất lượng món ăn, cùng hơn 200 món truyền thống và quốc tế.
            </p>
        </div>

        <!-- Phần thống kê -->
        <div class="grid grid-cols-1 md:grid-cols-4 bg-white">
            <div
                v-for="(item, i) in stats"
                :key="i"
                class="flex flex-col items-center justify-center py-10 px-4 text-center bg-cover bg-center h-64"
                :style="{ backgroundImage: `url(${item.bg})` }"
            >
                <h4 class="text-sm tracking-wider text-[#5a3e1b] font-semibold">
                    {{ item.label }}
                </h4>
                <p class="text-3xl font-bold text-[#5a3e1b] mt-2">
                    {{ item.value }}
                </p>
                <span class="text-xs text-[#5a3e1b] uppercase mt-1">{{
                    item.sub
                }}</span>
            </div>
        </div>
    </section>
</template>

<script setup>
import { defineComponent } from "vue";

// Có thể dùng icon FontAwesome hoặc Heroicons
const stats = [
    {
        icon: "1",
        label: "CHÚNG TÔI CÓ",
        value: "21",
        sub: "Sảnh",
        bg: "images/trainghiem_1.png",
    },
    {
        icon: "2",
        label: "DIỆN TÍCH",
        value: "12,675",
        sub: "m2",
        bg: "images/trainghiem_1.png",
    },
    {
        icon: "3",
        label: "ĐÃ TỔ CHỨC",
        value: "22,000",
        sub: "Tiệc cưới",
        bg: "images/trainghiem_1.png",
    },
    {
        icon: "4",
        label: "TỔ CHỨC",
        value: "7,268",
        sub: "Hội nghị và sự kiện",
        bg: "images/trainghiem_1.png",
    },
];
</script>

<style scoped>
/* Làm mờ ảnh nền như mẫu */
.bg-cover {
    background-size: cover;
    background-position: center;
    background-blend-mode: overlay;
    background-color: rgba(255, 255, 255, 0.6);
}
</style>
