<script lang="ts">
export default {
    components: {
        Header: () => import('~/components/header.vue'),
        Footer: () => import('~/components/footer.vue'),
    },
}
</script>

<template>
    <div>
        <Header />
        <slot />
        <Footer />
    </div>
</template>