<script setup lang="ts">
import { ref, watch } from 'vue';
import { useElementVisibility } from '@vueuse/core';

defineProps<{
    delay?: string
    duration?: string
}>();

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
    <div v-if="wasSeen" ref="target" :style="{animationDelay: delay, animationDuration: duration}" class="fade-in"><slot /></div>
    <div v-else ref="target"><slot /></div>
</template>

<style scoped>
    div {
        opacity: 0;
    }

    .fade-in {
        opacity: 0;
        animation: speed-in 1s ease-in-out 0.5s forwards;
    }

    @keyframes speed-in {
        0% {
            opacity: 0;
            transform: translateY(1rem);
        }

        100% {
            opacity: 1;
        }
    }
</style>