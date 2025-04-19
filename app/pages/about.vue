<template>
    <main>
        <section class="container py-20">
            <h1 class="text-3xl bold mb-6 text-balance">About Nuxtcipes:</h1>
            <p class="text-lg bold mb-6 text-balance max-w-screen-lg">
                Nuxtcipes is a recipe application based on the dummyJSON API,
                created by John Komarnicki for the
                <span class="font-bold">Build Modern Apps with Nuxt</span>
                course.
            </p>
            <NuxtLink to="/">
                <button
                    class="px-4 py-2 text-white self-start bg-amber-600/95 rounded-md text-xl hover"
                >
                    Back Home
                </button>
            </NuxtLink>
        </section>
    </main>
</template>

<script setup lang="ts"></script>
