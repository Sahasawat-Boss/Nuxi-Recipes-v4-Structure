<template>
    <header class="py-2.5 sm:py-4 border-b border-black/10">
        <nav class="flex flex-col sm:flex-row container px-4">
            <NuxtLink to="/" class="flex gap-1 items-center">
                <!-- <img class="w-14" src="public/icon-green.png" alt="icon" /> -->
                <NuxtImg width="40px" src="/icon-green.png" alt="icon" />
                <span class="text-xl md:text-3xl font-bold">Nuxi-Recipes</span>
            </NuxtLink>
            <ul
                class="flex gap-5.5 items-center ml-auto sm:text-lg font-bold capitalize"
            >
                <li>
                    <NuxtLink
                        to="/"
                        active-class="text-amber-600 underline"
                        exact-active-class="text-amber-600 underline"
                        >Home</NuxtLink
                    >
                </li>
                <li>
                    <NuxtLink
                        to="/about"
                        active-class="text-amber-600 underline"
                        exact-active-class="text-amber-600 underline"
                        >About</NuxtLink
                    >
                </li>
                <li>
                    <NuxtLink
                        to="/checklist"
                        active-class="text-amber-600 underline"
                        exact-active-class="text-amber-600 underline"
                        >Checklist</NuxtLink
                    >
                </li>
                <li>
                    <NuxtLink
                        to="/login"
                        active-class="text-amber-600 underline"
                        exact-active-class="text-amber-600 underline"
                        >Login</NuxtLink
                    >
                </li>
            </ul>
        </nav>
    </header>
</template>

<script setup lang="ts"></script>


<style scoped></style>