<script lang="ts">
import { wasteItems } from "~/data/wasteItems"
export default {
    data() {
        return {
            wasteItems
        }
    }
}
</script>

<template>
    <div class="flex flex-col justify-between gap-16 px-32 py-16">
        <h1 class="text-black capitalize text-center text-5xl">How to recycle them</h1>
        <div class="grid grid-rows-2 grid-flow-col gap-4">
            <div class="flex flex-col gap-2 justify-center align-middle items-start" v-for="item in wasteItems" :key="item.id">
                <h2 class="font-bold text-black text-2xl">{{ item.title }}</h2>
                <ul class="list-decimal text-black text-lg pl-4 justify-start items-start">
                    <li>{{ item.firstStep }}</li>
                    <li>{{ item.secondStep }}</li>
                    <li>{{ item.thirdStep }}</li>
                </ul>
            </div>
        </div>
    </div>
</template>