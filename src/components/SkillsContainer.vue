<script setup lang="ts">
import FadeInContainer from './FadeInContainer.vue';
import ThemeDiv from './ThemeDiv.vue';

const techSkills = ["Java", "Python", "C", "C++", "C#", "Javascript", "HTML", "CSS", "Postgresql", "R",
                    "Django", "NodeJs", "ReactJs", "Vue", "JQuery", "Git", "Unix"];
const softSkills = ["Problem-Solving", "Organization", "Time Management", "Communication"];
</script>

<template>
    <ThemeDiv main-color="var(--light-blue)" accent-color="var(--black)">
        <div class="skill-container">
            <FadeInContainer delay="0s">
                <h1>Skills</h1>
                <div class="skill-grid">
                    <div class="skill-col">
                        <h2>Technical Skills</h2>
                        <ul>
                            <li v-for="skill in techSkills">{{ skill }}</li>
                        </ul>
                    </div>
                    <div class="skill-col">
                        <h2>Soft Skills</h2>
                        <ul>
                            <li v-for="skill in softSkills">{{ skill }}</li>
                        </ul>
                    </div>
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

    .skill-col {
        
    }

    h1 {
        font-size: 3rem;
        font-weight: 200;
    }
</style>