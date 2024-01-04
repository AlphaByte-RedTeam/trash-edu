<script lang="ts">
const layout = () => import("~/layouts/default.vue")
// export default {
//   layout,
//   data() {
//     return {
//       layout: "default",
//     }
//   },
// }
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
