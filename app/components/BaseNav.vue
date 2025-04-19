<template>
    <header class="py-2.5 sm:py-4 border-b border-black/10">
        <nav class="flex flex-col sm:flex-row container px-4">
            <NuxtLink to="/" class="flex gap-1 items-center">
                <!-- <img class="w-14" src="public/icon-green.png" alt="icon" /> -->
                <NuxtImg width="45px" src="/icon-green.png" alt="icon" />
                <span class="text-3xl font-bold">Nuxi-Recipes</span>
            </NuxtLink>
            <ul class="flex gap-5.5 items-center ml-auto sm:text-lg font-bold capitalize">
                <li>
                    <NuxtLink to="/">Home</NuxtLink>
                </li>
                <li>
                    <NuxtLink to="/about">About</NuxtLink>
                </li>
                <li>
                    <NuxtLink to="/login">Login</NuxtLink>
                </li>
            </ul>
        </nav>
    </header>
</template>

<script setup lang="ts"></script>


<style scoped></style>