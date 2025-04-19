<template>
    <button
        v-show="showButton"
        @click="scrollToTop"
        class="fixed bottom-6 right-6 z-50 bg-amber-500 hover:bg-amber-600 text-white px-2 py-0 rounded-full text-3xl shadow-lg transition-all duration-300"
        aria-label="Scroll to top"
    >
        ↑
    </button>
</template>

<script setup lang="ts">
import { ref, onMounted, onUnmounted } from "vue";

const showButton = ref(false);

const handleScroll = () => {
    showButton.value = window.scrollY > 200;
};

const scrollToTop = () => {
    window.scrollTo({ top: 0, behavior: "smooth" });
};

onMounted(() => {
    window.addEventListener("scroll", handleScroll);
});

onUnmounted(() => {
    window.removeEventListener("scroll", handleScroll);
});
</script>
