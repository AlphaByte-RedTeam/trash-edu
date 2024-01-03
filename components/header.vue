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
    <div class="w-full py-6 px-32 text-2xl bg-secondary flex flex-row justify-between">
        <div class="logo flex flex-row gap-2">
            <NuxtImg src="/img/logo.svg" height="48" width="48"  />
            <p class="text-4xl text-accent font-bold">3R</p>
        </div>
        <div class="menus">
            <ul class="flex flex-row gap-8">
                <li class="text-accent font-medium" v-for="menuItem in menuItems" :key="menuItem.id">
                    <NuxtLink to="menuItem.path">
                        {{ menuItem.label }}
                    </NuxtLink>
                </li>
            </ul>
        </div>
    </div>
</template>