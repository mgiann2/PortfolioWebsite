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
    <div v-else ref="target"><slot /></div>
</template>

<style scoped>
    .speed-in {
        animation: speed-in 1s ease-in-out 0s ;
    }

    @keyframes speed-in {
        0% {
            transform: translateX(-100vw) skew(30deg);
        }

        70% {
            transform: translateX(-8vw) skew(30deg);
        }

        80% {
            transform: skew(-20deg);
        }

        90% {
            transform: skew(10deg);
        }

        100% {
            transform: skew(0deg);
        }
    }
</style>