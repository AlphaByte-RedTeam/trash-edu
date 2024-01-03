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
    <div class="w-full py-6 px-32 text-2xl m-0 sticky top-0 z-50 shadow-md bg-secondary flex flex-row justify-between">
        <Logo />
        <div class="menus">
            <ul class="flex flex-row gap-8">
                <li class="text-accent font-medium hover:underline hover:cursor-pointer" v-for="menuItem in menuItems" :key="menuItem.id">
                    <NuxtLink to="menuItem.path">
                        {{ menuItem.label }}
                    </NuxtLink>
                </li>
            </ul>
        </div>
    </div>
</template>