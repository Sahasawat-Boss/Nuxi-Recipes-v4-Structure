<template>
    <main>
        <section class="container py-20 px-6">
            <h1 class="text-3xl bold mb-6 text-balance">About Nuxtcipes:</h1>
            <p class="text-lg mb-6 text-balance ">
                Nuxtcipes is a recipe application based on the dummyJSON API,
                created by John Komarnicki for the
                <span class="font-bold">Build Modern Apps with Nuxt</span>
                course.
            </p>
            <NuxtLink to="/">
                <button
                    class="px-4 py-2 text-white self-start bg-amber-600/95 rounded-md text-lg hover"
                >
                    Back Home
                </button>
            </NuxtLink>
        </section>
    </main>
</template>

<script setup lang="ts"></script>
