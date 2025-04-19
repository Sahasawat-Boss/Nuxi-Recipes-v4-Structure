<template>
    <div>
        <section class="bg-[#f1f1f1]">
            <div
                class="container flex flex-col lg:flex-row items-center py-12 px-10 gap-10"
            >
                <div class="flex-1 order-2 lg:order-2 text-center lg:text-left">
                    <h1
                        class="text-4xl lg:text-5xl font-bold mb-12 text-balance"
                    >
                        Login Page Test
                    </h1>
                    <NuxtLink to="/">
                        <button
                            class="px-4 py-2 text-white self-start bg-amber-600/95 rounded-md text-xl hover"
                        >
                            Back Home
                        </button>
                    </NuxtLink>
                </div>
                <div class="flex-1 order-1 lg:order-1">
                    <NuxtImg
                        sizes="50vw md:400px"
                        src="/nuxt-course-hero.png"
                        format="webp"
                        densities="x1"
                        alt="hero image"
                        class="spin rotate-200 drop-shadow-lg drop-shadow-green-700/30"
                    />
                </div>
            </div>
        </section>
    </div>
</template>

    <script lang="ts" setup>
definePageMeta({
    layout: "login",
});
</script>

<style></style>