<script setup lang="ts">
import { ref, watch } from 'vue';
import { useElementVisibility } from '@vueuse/core';

const target = ref(null);
const isVisible = useElementVisibility(target);
const wasSeen = ref(false);

watch(isVisible, async (newIsVisible) => {
    if (newIsVisible) {
        wasSeen.value = true;
    }
})
</script>

<template>
    <div v-if="wasSeen" ref="target" class="speed-in"><slot /></div>
    <div style="opacity: 0;" v-else ref="target"><slot /></div>
</template>

<style scoped>
    .speed-in {
        transform: translate(0);
        animation: speed-in 0.8s ease-in-out 0s forwards;
    }

    @keyframes speed-in {
        0% {
            transform: translateX(-100vw) skewX(30deg);
        }

        70% {
            transform: translateX(0) skewX(10deg);
        }

        80% {
            transform: skewX(-30deg);
        }

        90% {
            transform: skewX(10deg);
        }

        100% {
            transform: skewX(0deg);
        }
    }
</style>