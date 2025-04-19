<template>
    <!-- Hero Section -->
    <section class="bg-[#f1f1f1]">
        <div
            class="container flex flex-col lg:flex-row items-center py-12 px-10 gap-10"
        >
            <div class="flex-1 order-2 lg:order-1 text-center lg:text-left">
                <h1 class="text-4xl lg:text-5xl font-bold mb-6 text-balance fade-left">
                    Cook Like a Pro at Home
                </h1>
                <p class="text-xl lg:text-2xl mb-8 text-balance fade-right">
                    Easy, tasty recipes that make cooking fun and stress-free.
                </p>

                <NuxtLink to="#all-recipe">
                    <button
                        class="btn-pri fade-up"
                    >
                        Browse Recipes
                    </button>
                </NuxtLink>
            </div>
            <div class="flex-1 order-1 lg:order-2">
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
</template>