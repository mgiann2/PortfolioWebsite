<script setup lang="ts">

defineProps<{
    mainColor?: string
    accentColor?: string 
}>();

</script>

<template>
    <div class="main" :style="{backgroundColor: mainColor}">
        <div class="top-left-accent" :style="{borderColor: accentColor}"></div>
        <div class="bottom-right-accent" :style="{borderColor: accentColor}"></div>
        <div><slot/></div>
    </div>
</template>

<style>
    .main {
        position: relative;
        min-height: 300px;
        padding: 2rem;
    }

    .top-left-accent {
        position: absolute;
        top: 1rem;
        left: 1rem;
        width: 80px;
        height: 50px;
        border-top: solid 15px var(--light-green);
        border-left: solid 15px var(--light-green);
    }

    .bottom-right-accent {
        position: absolute;
        bottom: 1rem;
        right: 1rem;
        width: 80px;
        height: 50px;
        border-bottom: solid 15px var(--light-green);
        border-right: solid 15px var(--light-green);
    }
</style>