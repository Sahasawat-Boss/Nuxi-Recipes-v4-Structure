<template>
    <header class="py-4 border-b border-black/10">
        <nav class="flex container items-center">
            <NuxtLink to="/" class="flex gap-1 items-center">
                <!-- <img class="w-14" src="public/icon-green.png" alt="icon" /> -->
                <NuxtImg width="56px" src="/icon-green.png" alt="icon" />
                <span class="text-3xl font-bold">Nuxtcipes</span>
            </NuxtLink>
            <ul class="flex gap-6 ml-auto text-xl font-bold capitalize">
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