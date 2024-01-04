<script lang="ts">
const layout = () => import("~/layouts/default.vue")
const Hero = () => import("~/components/hero.vue")
const WatchVideo = () => import("~/components/watchVideo.vue")
const WasteTypes = () => import("~/components/wasteTypes.vue")
const WasteSort = () => import("~/components/wasteSort.vue")
export default {
  layout,
  components: {
    Hero,
    WatchVideo,
    WasteTypes,
    WasteSort,
  },
  data() {
    return {
      layout: "default",
    }
  },
}
</script>

<template>
  <div class="flex flex-col justify-between min-h-screen bg-primary">
    <NuxtLayout :name="layout">
      <div id="content">
        <Hero />
        <WatchVideo />
        <WasteTypes />
        <WasteSort />
      </div>
    </NuxtLayout>
  </div>
</template>
