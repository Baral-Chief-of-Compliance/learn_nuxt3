<script setup>
const { $hello } = useNuxtApp()
console.log(useNuxtApp())
</script>

<template>
    <div>index page</div>
    <div>
        <ContentDoc />
    </div>
    
    <div class="Main">
        <HeaderComponent />
        <Alert />
        <div>
            {{ $hello('world') }}
        </div>

        <img src="@/assets/nasa.png" width="100" alt="NasaLogo"/>
        <img src="@/assets/nasa_2.png" width="100" alt="NasaLogo2"/>
        <img src="/nasa_2.png" width="100" alt="NasaLogo2Public"/>

    </div>
</template>

<style lang="scss"></style>