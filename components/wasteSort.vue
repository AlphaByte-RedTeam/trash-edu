<script lang="ts">
import draggable from "vuedraggable";
import { wasteSortItems } from "~/data/wasteSortItems"
export default {
    data() {
        return {
            list1: wasteSortItems,
            list2: [],
        }
    },
    components: {
        draggable,
    },
    methods: {
        log: function (evt: String) {
            window.console.log(evt);
        }
    }
}
</script>

<template>
    <div class="px-32 flex flex-row pb-8 justify-between">
        <div class="flex flex-col">
            <h1 class="text-center font-bold text-xl bg-white text-black py-2">Waste Items</h1>
            <dragggable class="bg-secondary w-48" group="wastes" :list="list1" @change="log">
                <div v-for="item in list1" :key="item.id">
                    <WasteSortCard
                        :waste-name="item.labelName"
                        :waste-material="item.material"
                        :waste-color="item.bgColor"
                    />
                </div>
            </dragggable>
        </div>
        <div class="flex flex-col">
            <h1 class="text-center font-bold text-xl bg-[#606264] text-white py-2">Organic Trash Bin</h1>
            <dragggable class="bg-secondary w-48" group="items" :list="list1" @change="log">
                <!-- <div v-for="item in list2" :key="item.id">
                    <WasteSortCard
                        :waste-name="item.labelName"
                        :waste-material="item.material"
                        :waste-color="item.bgColor"
                    />
                </div> -->
            </dragggable>
        </div>
        <div class="flex flex-col">
            <h1 class="text-center font-bold text-xl bg-[#FF9D06] text-white py-2">Plastic Trash Bin</h1>
            <dragggable class="bg-secondary w-48" group="items" :list="list1" @change="log">
                <!-- <div v-for="item in list2" :key="item.id">
                    <WasteSortCard
                        :waste-name="item.labelName"
                        :waste-material="item.material"
                        :waste-color="item.bgColor"
                    />
                </div> -->
            </dragggable>
        </div>
        <div class="flex flex-col">
            <h1 class="text-center font-bold text-xl bg-[#008BCA] text-white py-2">Paper Trash Bin</h1>
            <dragggable class="bg-secondary w-48" group="items" :list="list1" @change="log">
                <!-- <div v-for="item in list2" :key="item.id">
                    <WasteSortCard
                        :waste-name="item.labelName"
                        :waste-material="item.material"
                        :waste-color="item.bgColor"
                    />
                </div> -->
            </dragggable>
        </div>
        <div class="flex flex-col">
            <h1 class="text-center font-bold text-xl bg-[#02CE6F] text-white py-2">Glass Trash Bin</h1>
            <dragggable class="bg-secondary w-48" group="items" :list="list1" @change="log">
                <!-- <div v-for="item in list2" :key="item.id">
                    <WasteSortCard
                        :waste-name="item.labelName"
                        :waste-material="item.material"
                        :waste-color="item.bgColor"
                    />
                </div> -->
            </dragggable>
        </div>
    </div>
</template>

<!-- Reference: https://sortablejs.github.io/Vue.Draggable/#/two-lists -->