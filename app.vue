<script lang="ts">
const layout = () => import("~/layouts/default.vue")
</script>

<template>
  <div class="flex flex-col justify-between min-h-screen bg-primary">
    <NuxtLayout :name="layout">
      <div id="content">
        <Hero />
        <WatchVideo />
        <WasteTypes />
      </div>
    </NuxtLayout>
  </div>
</template>
