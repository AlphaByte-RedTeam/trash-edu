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
    <div class="px-32 py-16 flex flex-col justify-center gap-8 align-middle items-center">
        <h1 class="capitalize text-5xl text-center">Different Types Of Waste</h1>
        <div class="grid grid-rows-2 grid-flow-col gap-4">
            <WasteCard v-for="wasteItem in wasteItems" :key="wasteItem.id" :bg-color="wasteItem.bgColor" :title="wasteItem.title" :img-src="wasteItem.img" :title-name="wasteItem.title" :desc="wasteItem.desc" />
        </div>
    </div>
</template>