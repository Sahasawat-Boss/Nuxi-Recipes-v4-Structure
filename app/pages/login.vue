<template>
    <div>
        <section class="bg-[#f1f1f1]">
            <div
                class="container flex flex-col lg:flex-row items-center py-12 px-10 gap-10"
            >
                <!-- Text Content -->
                <div class="flex-1 order-2 lg:order-2 text-center lg:text-left">
                    <h1
                        class="text-4xl lg:text-5xl font-bold mb-6 text-balance fade-left"
                    >
                        Login Page Coming Soon 🚧
                    </h1>
                    <p class="text-lg lg:text-xl text-gray-600 mb-12 fade-in">
                        We’re working hard to bring you a secure and seamless
                        login experience. Stay tuned!
                    </p>
                    <NuxtLink to="/">
                        <button class="btn-pri fade-up">Back to Home</button>
                    </NuxtLink>
                </div>

                <!-- Image -->
                <div class="flex-1 order-1 lg:order-1">
                    <NuxtImg
                        sizes="30vw md:400px"
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

useSeoMeta({
    title: "Nuxi Recipes | Login",
});
</script>

<style></style>