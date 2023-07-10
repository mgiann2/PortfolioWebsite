<script setup lang="ts">
import FadeInContainer from './FadeInContainer.vue';
import ThemeDiv from './ThemeDiv.vue';

const skills = ["Java", "Python", "C", "C++", "C#", "Javascript", "HTML", "CSS", "Postgresql", "R",
                    "Django", "NodeJs", "ReactJs", "Vue", "JQuery", "Git", "Unix"];
</script>

<template>
    <ThemeDiv main-color="var(--light-blue)" accent-color="var(--black)">
        <div class="skill-container">
            <FadeInContainer delay="0s">
                <h1>Skills</h1>
                <div class="skill-grid">
                    <span class="skill-span" v-for="skill in skills">{{ skill }}</span>
                </div>
            </FadeInContainer>
        </div>
    </ThemeDiv>
</template>

<style scoped>
    .skill-container {
        padding: 1.5rem 20%;
        color: var(--black);
    }

    .skill-grid {
        display: flex;
        flex-wrap: wrap;
        justify-content: space-around;
    }

    .skill-span {
        width: 10rem;
        margin: 0.3rem 0;
        text-align: center;
        font-size: large;
    }

    h1 {
        font-size: 3rem;
        font-weight: 200;
        text-align: center;
    }
</style>