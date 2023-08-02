<template>
    <main id="app-container">
        <!-- ThreeDBackground -->
        <LoadingSpinner v-if="!loaded" />
        <Login />
    </main>
</template>

<script lang="ts" setup>

let loaded = true

</script>

<style lang="scss">
body,
html {
    overflow: hidden;
    height: 100vh;
    width: 100vw;
}

#app-container {
    background-color: black;
    height: 100vh;
    width: 100vw;
    overflow: hidden;
}
</style>