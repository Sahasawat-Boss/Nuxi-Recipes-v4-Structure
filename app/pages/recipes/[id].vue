<template>
    <section class="p-2">
        <NuxtLink to="/">
            <button
                class="px-2.5 py-1 text-white self-start bg-amber-600/95 rounded-md text-sm hover"
            >
                Back Home
            </button>
        </NuxtLink>
    </section>
    <div class="flex flex-col max-w-screen-lg container px-10 py-8">
        <!-- Header -->
        <div class="flex flex-col mb-6">
            <h2 class="text-2xl md:text-5xl mb-4 font-semibold">
                {{ data?.name }}
            </h2>
            <div class="flex gap-4 text-xl mb-6">
                <div class="flex items-center gap-1">
                    <Icon
                        name="mdi:clock-time-eight-outline"
                        style="color: #f79f1a"
                    />
                    <span>{{ data?.cookTimeMinutes }}</span>
                </div>
                <div class="flex items-center gap-1">
                    <Icon name="mdi:fire" style="color: #f79f1a" />
                    <span>{{ data?.caloriesPerServing }}</span>
                </div>
                <div class="flex items-center gap-1">
                    <Icon name="mdi:star" style="color: #f79f1a" />
                    <span>{{ data?.rating }} ({{ data?.reviewCount }})</span>
                </div>
            </div>
            <hr />
        </div>

        <!-- Image -->
        <NuxtImg
            :src="data?.image"
            densities="x1"
            sizes="xs:100vw sm:100vw md:100vw lg:100vw"
            class="w-full max-h-[500px] object-cover rounded-md shadow-sm mb-12"
            alt=""
        />

        <!-- Ingredients -->
        <div class="mb-8">
            <h2 class="text-2xl font-semibold mb-4">Ingredients</h2>
            <ul class="grid grid-cols-1 md:grid-cols-2 gap-2 text-lg">
                <li v-for="ingredient in data?.ingredients" :key="ingredient">
                    <!-- don't use an id like ingredient.id as the :key Because ingredient is just a string, not an object-->
                    <label class="flex gap-2 items-center">
                        <input class="hidden peer" type="checkbox" />
                        <div
                            class="relative w-6 h-6 rounded-full border-2 border-dodgeroll-gold flex items-center justify-center peer-checked:after:absolute peer-checked:after:w-4 peer-checked:after:h-4 peer-checked:after:bg-amber-500 peer-checked:after:rounded-full"
                        ></div>
                        <span class="peer-checked:line-through">
                            {{ ingredient }}
                        </span>
                    </label>
                </li>
            </ul>
        </div>

        <!-- Instructions -->
        <div>
            <h2 class="text-2xl bold mb-4">Instructions</h2>
            <ul class="flex flex-col text-lg gap-4">
                <li
                    v-for="(instruction, index) in data?.instructions"
                    :key="instruction"
                    class="flex gap-2"
                >
                    <span
                        class="flex items-center justify-center bg-amber-500 w-7 h-7 rounded-full text-white text-sm"
                    >
                        {{ index + 1 }}
                    </span>
                    <span class="flex-1">{{ instruction }}</span>
                </li>
            </ul>
        </div>
    </div>
</template>

<script lang="ts" setup>
import { type RecipeRes } from "../../../types/types";

const route = useRoute();
const recipeId = Number(route.params.id);

const { data: rawData, error } = await useFetch<RecipeRes>(
    "https://dummyjson.com/recipes?limit=20"
);

// Find the matching recipe from the list
const data = computed(() => {
    return rawData.value?.recipes.find((r: any) => r.id === recipeId);
});

if (error.value) {
    throw createError({
        status: error.value?.statusCode,
        statusText: error.value?.statusMessage,
    });
}
</script>

<style scoped>
</style>