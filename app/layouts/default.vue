<template>
    <div>
        <BaseNav />
        <slot />
        <hr class="mt-12 border-t border-gray-300" />
        <h1 class="text-center py-2">Default Layout</h1>
    </div>
</template>

<script setup lang="ts">
useSeoMeta({
    title: "Nuxi Recipes",
    description: "Welcome to my Nuxt 3 site.",
    ogTitle: "My Awesome Nuxt App",
    ogDescription: "Explore amazing recipes with Nuxt 3.",
    ogImage: "/nuxt-course-hero.png",
    ogUrl: "https://yourdomain.com",
    twitterTitle: "My Awesome Nuxt App",
    twitterDescription: "Try out these beginner-friendly recipes.",
    twitterImage: "/nuxt-course-hero.png",
    twitterCard: "summary_large_image",
});

useHead({
    htmlAttrs: {
        lang: "en",
    },
    link: [
        {
            rel: "icon",
            type: "image/png",
            href: "/favicon.ico",
        },
    ],
});
</script>
