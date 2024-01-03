<script lang="ts">
export default {
    props: {
        titleName: {
            type: String,
            required: true
        },
        desc: {
            type: String,
            required: true
        },
        imgSrc: {
            type: String,
            required: true
        },
        bgColor: {
            type: String,
            required: true
        },
    },
}
</script>

<template>
    <div class="flex flex-row gap-6 p-4 justify-center items-center rounded-2xl w-[616px] h-[268px] bg-[#606264]" :style="{ backgroundColor: bgColor }">
        <NuxtImg :src="imgSrc"  height="150" />
        <div class="flex flex-col gap-4 text-white">
            <h2 class="text-3xl font-semibold">{{ titleName }}</h2>
            <p class="text-lg">{{ desc }}</p>
        </div>
    </div>
</template>