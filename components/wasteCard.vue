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
        step1: {
            type: String,
            required: true
        },
        step2: {
            type: String,
            required: true
        },
        step3: {
            type: String,
            required: true
        },
    },
}
</script>

<template>
    <DialogRoot>
        <DialogTrigger>
            <div class="flex flex-row gap-6 p-4 justify-center items-center rounded-2xl w-[616px] h-[268px] bg-[#606264]" :style="{ backgroundColor: bgColor }">
                <NuxtImg :src="imgSrc"  height="150" />
                <div class="flex flex-col gap-4 text-white">
                    <h2 class="text-3xl font-semibold">{{ titleName }}</h2>
                    <p class="text-lg">{{ desc }}</p>
                </div>
            </div>
        </DialogTrigger>
        <DialogPortal>
            <DialogOverlay class="backdrop-blur-md data-[state=open]:animate-overlayShow fixed inset-0 z-30" />
            <DialogContent class="data-[state=open]:animate-contentShow fixed top-[50%] left-[50%] max-h-[85vh] w-[90vw] max-w-[500px] translate-x-[-50%] translate-y-[-50%] rounded-[6px] bg-white p-[25px] shadow-[hsl(206_22%_7%_/_35%)_0px_10px_38px_-10px,_hsl(206_22%_7%_/_20%)_0px_10px_20px_-15px] focus:outline-none z-[100]">
                <DialogTitle class="text-secondary mb-2 text-xl text-center font-semibold">Recycling {{ titleName }}</DialogTitle>
                <DialogDescription class="text-green-900 text-base">
                    <ul style="list-style: circle;" class="flex flex-col gap-2 ml-4">
                        <li>{{ step1 }}</li>
                        <li>{{ step2 }}</li>
                        <li>{{ step3 }}</li>
                    </ul>
                </DialogDescription>
                <DialogClose
                    class="text-grass11 hover:bg-green4 focus:shadow-green7 absolute top-[10px] right-[10px] inline-flex h-[25px] w-[25px] appearance-none items-center justify-center rounded-full focus:shadow-[0_0_0_2px] focus:outline-none"
                    aria-label="Close"
                >
                </DialogClose>
            </DialogContent>
        </DialogPortal>
    </DialogRoot>
</template>