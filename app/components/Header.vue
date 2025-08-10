<template>
    <header class="bg-white shadow-sm sticky top-0 z-50">
        <div
            class="max-w-7xl mx-auto flex items-center justify-between px-6 py-4"
        >
            <!-- Logo -->
            <div class="flex items-center space-x-3">
                <img
                    src="/images/avt_1.png"
                    alt="phu giao WEDDING"
                    class="h-10"
                />
                <span
                    class="text-[#B4995A] font-semibold tracking-wide text-sm"
                >
                    PHÚ GIÁO WEDDING
                </span>
            </div>

            <!-- Hamburger button (mobile) -->
            <button
                @click="isOpen = !isOpen"
                class="md:hidden text-gray-700 focus:outline-none"
            >
                <i
                    class="fa-solid"
                    :class="isOpen ? 'fa-xmark' : 'fa-bars'"
                ></i>
            </button>

            <!-- Menu (desktop) -->
            <nav class="hidden md:flex space-x-8 text-sm font-medium">
                <NuxtLink
                    to="/"
                    class="px-4 py-2 rounded-md transition-colors"
                    :class="{ 'bg-[#B4995A] text-white': isActive('/') }"
                >
                    TRANG CHỦ
                </NuxtLink>
                <NuxtLink to="/" class="px-4 py-2 rounded-md transition-colors"
                    >TIỆC CƯỚI</NuxtLink
                >
                <NuxtLink to="/" class="px-4 py-2 rounded-md transition-colors"
                    >HỘI NGHỊ</NuxtLink
                >
                <NuxtLink to="/" class="px-4 py-2 rounded-md transition-colors"
                    >THƯ VIỆN</NuxtLink
                >
                <NuxtLink to="/" class="px-4 py-2 rounded-md transition-colors"
                    >TIN TỨC</NuxtLink
                >
                <NuxtLink to="/" class="px-4 py-2 rounded-md transition-colors"
                    >LIÊN HỆ</NuxtLink
                >
            </nav>
        </div>

        <!-- Mobile dropdown menu -->
        <div v-if="isOpen" class="md:hidden bg-white border-t border-gray-200">
            <nav class="flex flex-col text-sm font-medium">
                <NuxtLink
                    to="/"
                    class="px-6 py-3 hover:bg-gray-100"
                    :class="{ 'bg-[#B4995A] text-white': isActive('/') }"
                    @click="isOpen = false"
                >
                    TRANG CHỦ
                </NuxtLink>
                <NuxtLink
                    to="/"
                    class="px-6 py-3 hover:bg-gray-100"
                    @click="isOpen = false"
                >
                    TIỆC CƯỚI
                </NuxtLink>
                <NuxtLink
                    to="/"
                    class="px-6 py-3 hover:bg-gray-100"
                    @click="isOpen = false"
                >
                    HỘI NGHỊ
                </NuxtLink>
                <NuxtLink
                    to="/"
                    class="px-6 py-3 hover:bg-gray-100"
                    @click="isOpen = false"
                >
                    THƯ VIỆN
                </NuxtLink>
                <NuxtLink
                    to="/"
                    class="px-6 py-3 hover:bg-gray-100"
                    @click="isOpen = false"
                >
                    TIN TỨC
                </NuxtLink>
                <NuxtLink
                    to="/"
                    class="px-6 py-3 hover:bg-gray-100"
                    @click="isOpen = false"
                >
                    LIÊN HỆ
                </NuxtLink>
            </nav>
        </div>
    </header>
</template>

<script setup>
import { ref } from "vue";
import { useRoute } from "vue-router";

const route = useRoute();
const isActive = (path) => route.path === path;
const isOpen = ref(false);
</script>

<style>
@import url("https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css");
</style>
