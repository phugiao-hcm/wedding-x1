<template>
    <section class="bg-[#f7f1e8] py-12">
        <!-- Tiêu đề -->
        <div class="text-center mb-10">
            <h3 class="text-[#b4995a] italic text-2xl">Trải nghiệm</h3>
            <h2 class="text-4xl font-bold text-[#5a3e1b]">KHÔNG GIAN</h2>
            <p class="text-[#b4995a] italic mt-1">Đẳng cấp</p>
        </div>

        <!-- Hình ảnh -->
        <div
            class="max-w-10xl mx-auto grid grid-cols-1 md:grid-cols-2 gap-6 px-4"
        >
            <div>
                <img
                    src="/images/trainghiem_1.png"
                    alt="Không gian 1"
                    class="w-full h-auto object-cover"
                />
            </div>
            <div>
                <img
                    src="/images/trainghiem_2.png"
                    alt="Không gian 2"
                    class="w-full h-auto object-cover"
                />
            </div>
        </div>
    </section>
</template>

<script setup>
// Không cần JS phức tạp, chỉ là layout tĩnh
</script>

<style scoped>
/* Nếu muốn ảnh bo góc như hình */
img {
    border-radius: 4px;
}
</style>
