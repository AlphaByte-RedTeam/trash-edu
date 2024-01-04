<script lang="ts">
export default {
    props: {
        wasteName: {
            type: String,
            required: true
        },
        wasteMaterial: {
            type: String,
            required: true
        },
        wasteColor: {
            type: String,
            required: true
        },
    },
}
</script>

<template>
    <div class="flex flex-col gap-4 py-2 px-2">
        <div class="rounded-lg px-2 py-1 border border-white flex flex-col gap-1 justify-center items-start text-white" :style="{ backgroundColor: wasteColor }">
            <h2 class="font-bold text-lg">{{ wasteName }}</h2>
            <p class="font-normal text-base">Material: {{ wasteMaterial }}</p>
        </div>
    </div>
</template>