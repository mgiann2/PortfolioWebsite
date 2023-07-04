<script setup lang="ts">
import ThemeDiv from './ThemeDiv.vue';
import FadeInContainer from './FadeInContainer.vue';
import ProjectCard from './ProjectCard.vue';

interface Project {
    name: string;
    description: string;
    skillsUsed: string[];
    image: string;
}
</script>

<template>
    <ThemeDiv >
        <FadeInContainer>
            <div class="project-container">
                <h1 style="margin: 0;">Projects</h1>
            </div>
            <div class="project-grid">
                <ProjectCard />
                <ProjectCard />
                <ProjectCard />
                <ProjectCard />
                <ProjectCard />
                <ProjectCard />
            </div>
        </FadeInContainer>
    </ThemeDiv>
</template>

<style scoped>
    .project-container {
        padding: 1.5rem 20%;
    }

    .project-grid {
        padding: 0 10%;
        display: flex;
        flex-wrap: wrap;
        gap: 1em;
        align-items: left;
        justify-content: space-around;
    }

    h1 {
        font-size: 3rem;
        font-weight: 200;
    }
</style>