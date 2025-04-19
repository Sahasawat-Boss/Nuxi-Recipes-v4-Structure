<template>
    <main>
        <section class="container py-12 px-6">
            <h1 class="text-3xl bold mb-6 text-balance fade-right">About Nuxtcipes:</h1>
            <p class="text-lg mb-6 text-balance fade-left">
                Nuxtcipes is a modern recipe application originally built by
                <span class="font-bold"> John Komarnicki </span> as part of the
                Build Modern Apps with Nuxt course. It integrates with the
                <span class="font-bold"> DummyJSON Recipes API </span>
                to showcase recipe listings, detail pages, and more.
                <br /><br />
                This version has been upgraded and enhanced by
                <span class="font-bold">Sahasawat (Boss)</span>
                with the latest features and improvements including: Improved
                responsive layout SEO enhancements using useSeoMeta()
                Interactive ingredient checklist & todo list Optimized
                lazy-loaded images with NuxtImg Smooth scrolling and UI
                refinements
            </p>
            <NuxtLink to="/">
                <button
                    class="btn-pri fade-up"
                >
                    Back Home
                </button>
            </NuxtLink>
        </section>
    </main>
</template>

<script setup lang="ts">
useSeoMeta({
    title: "Nuxi Recipes | About",
});
</script>
