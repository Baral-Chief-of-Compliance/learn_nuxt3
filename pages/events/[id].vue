<script setup>
    const route = useRoute();
    const nuxt = useNuxtApp()

    console.log(route.params.id)
    console.log(nuxt)
</script>

<template>
    <div>event id: {{ this.$route.params.id }}</div>
</template>