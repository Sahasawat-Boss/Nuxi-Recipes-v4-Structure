<template>
    <!-- Hero Section -->
    <section class="bg-[#f1f1f1]">
        <div
            class="container flex flex-col lg:flex-row items-center py-12 px-10 gap-10"
        >
            <div class="flex-1 order-2 lg:order-1 text-center lg:text-left">
                <h1 class="text-4xl lg:text-5xl font-bold mb-6 text-balance">
                    Cook Like a Pro at Home
                </h1>
                <p class="text-xl lg:text-2xl mb-8 text-balance">
                    Easy, tasty recipes that make cooking fun and stress-free.
                </p>

                <NuxtLink
                    to="#all-recipe"
                    class="px-4 py-2 text-white self-start bg-amber-600/95 rounded-md text-lg hover"
                >
                    Browse Recipes
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