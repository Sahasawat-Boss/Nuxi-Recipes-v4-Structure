<template>
    <main>
        <HeroSection />

        <!-- Fetch Recipe Data -->
        <section class="py-16 px-10 container fade-in " id="all-recipe">
            <h2 class="text-3xl mb-2 font-bold">Top Picks for You</h2>
            <p class="text-lg lg:text-xl mb-8">
                Explore our most-loved recipes!
            </p>

            <!-- Display Recipes -->
            <div
                class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-x-4 gap-y-8"
            >
                <div
                    v-for="recipes in data?.recipes"
                    :key="recipes.id"
                    class="flex flex-col shadow rounded-md"
                >
                    <!-- :key is important for performance, correctness, and avoiding subtle bugs in Vue. -->
                    <NuxtImg
                        :src="recipes.image"
                        format="webp"
                        sizes="100vw lg:400px"
                        densities="x1"
                        alt="recipes image"
                        loading="lazy"
                        placeholder="blur"    
                        class="rounded-t-xl w-full"
                    />
                    <div class="flex flex-col py-6 px-4 flex-1">
                        <p class="text-xl lg:text-2xl font-semibold mb-2">
                            {{ recipes.name }}
                        </p>
                        <div
                            class="font-normal w-full bg-white/80 flex gap-8 text-lg lg:text-xl mb-4 mt-auto"
                        >
                            <!-- <Icon name="material-symbols:clock-loader-10" width="24" height="24" class="text-red-500"/> -->
                            <!-- Icon from https://icon-sets.iconify.design/material-symbols/?icon-filter=clock have to change icon= >> to name= -->

                            <div class="flex flex-col items-center gap-1">
                                <Icon
                                    name="mdi:clock-time-eight-outline"
                                    style="color: #f79f1a"
                                />
                                <span class="text-xs text-black/55"
                                    >Cook Time</span
                                >
                                <span class="font-semibold">{{
                                    recipes.cookTimeMinutes
                                }}</span>
                            </div>
                            <div class="flex flex-col items-center gap-1">
                                <Icon name="mdi:fire" style="color: #f79f1a" />
                                <span class="text-xs text-black/55"
                                    >Calories</span
                                >
                                <span class="font-semibold">{{
                                    recipes.caloriesPerServing
                                }}</span>
                            </div>
                            <div class="flex flex-col items-center gap-1">
                                <Icon name="mdi:star" style="color: #f79f1a" />
                                <span class="text-xs text-black/55"
                                    >Rating</span
                                >
                                <span class="font-semibold">{{
                                    recipes.rating
                                }}</span>
                            </div>
                        </div>
                        <NuxtLink
                            :to="`/recipes/${recipes.id}`"
                            class="btn-pri scale-85"
                        >
                            View
                        </NuxtLink>
                    </div>
                </div>
            </div>
        </section>

        <ScrollUp/>
    </main>
</template>

<script lang="ts" setup>
// const { data, error } = useAsyncData('recipes',() => $fetch("https://dummyjson.com/recipes?limit=12") );

import { type RecipeRes } from "../../types/types";

const { data, error } = await useFetch<RecipeRes>(
    "https://dummyjson.com/recipes?limit=20"
);

useSeoMeta({
    title: "Nuxi Recipes | Home",
});
</script>
