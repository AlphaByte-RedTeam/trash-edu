<script lang="ts">
import { menuItems } from "~/data/menuItems"

export default {
    data() {
        return {
            menuItems
        }
    }
}
</script>

<template>
    <div class="flex flex-row px-32 justify-between py-16 bg-secondary w-full">
        <div class="flex flex-row justify-between w-3/5 align-top">
            <div id="brand-identity" class="flex flex-col gap-4">
                <Logo />
                <p class="text-base text-accent w-64">
                    Jalan Lodan Raya No. 2, Ancol, Pademangan, RT.12/RW.2, Kota Tua, Ancol, Pademangan, Kota Jakarta Utara
                </p>
            </div>
            <div id="kelompok" class="flex flex-col gap-4 text-accent">
                <h1 class="text-2xl font-semibold">Kelompok 7</h1>
                <ul id="anggota" class="flex flex-col gap text-base">
                    <li>Andrew Virya Victorio - 32200091</li>
                    <li>Janice Claresta Lingga - 32200041</li>
                    <li>Feri Andika - 32200007</li>
                    <li>Chandra Medhika - 32200033</li>
                </ul>
            </div>
            <div id="resources" class="flex flex-col gap-4 text-accent">
                <h1 class="text-2xl font-semibold">Resources</h1>
                <ul id="resource-list" class="flex flex-col gap text-base">
                    <li>
                        Illustrations by 
                        <NuxtLink to="https://freepik.com" class="hover:cursor-pointer hover:underline hover:transition hover:ease-in-out hover:duration-300" target="_blank">Freepik</NuxtLink>
                    </li>
                    <li>
                        Videos from
                        <NuxtLink to="https://www.youtube.com/watch?v=6jQ7y_qQYUA" class="hover:cursor-pointer hover:underline hover:transition hover:ease-in-out hover:duration-300" target="_blank">YouTube</NuxtLink>
                    </li>
                </ul>
            </div>
            <div id="sections" class="flex flex-col gap-4 text-accent">
                <h1 class="text-2xl font-semibold">Sections</h1>
                <ul id="section-list" class="flex flex-col gap text-base">
                    <li v-for="menuItem in menuItems" :key="menuItem.id">
                        <NuxtLink to="menuItem.path" class="hover:cursor-pointer hover:underline">
                            {{ menuItem.label }}
                        </NuxtLink>
                    </li>
                </ul>
            </div>
        </div>
        <div class="flex flex-col justify-center gap-2">
            <NuxtLink target="_blank" to="https://vercel.com" class="hover:cursor-pointer hover:-translate-y-1 hover:transition-all hover:duration-300 hover:ease-in-out">
                <div id="vercel" class="flex flex-row justify-center gap-2 p-4 bg-white rounded-lg w-[256px]">
                    <span class="font-medium text-lg">Deployed To</span>
                    <NuxtImg src="/img/vercel.svg" height="96" width="96" />
                </div>
            </NuxtLink>
            <NuxtLink target="_blank" to="https://nuxt.com" class="hover:cursor-pointer hover:-translate-y-1 hover:transition-all hover:duration-300 hover:ease-in-out">
                <div id="vercel" class="flex flex-row justify-center gap-2 p-4 bg-white rounded-lg w-[256px]">
                    <span class="font-medium text-lg">Made With</span>
                    <NuxtImg src="/img/nuxt.svg" height="96" width="96" />
                </div>
            </NuxtLink>
        </div>
    </div>
</template>