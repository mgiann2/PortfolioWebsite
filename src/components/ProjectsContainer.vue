<script setup lang="ts">
import ThemeDiv from './ThemeDiv.vue';
import FadeInContainer from './FadeInContainer.vue';
import ProjectCard from './ProjectCard.vue';
import { type Project } from '../helper';
import anovaImg from '../assets/anova-website.png';
import sudokuImg from '../assets/sudoku-website.png';

const projects: Project[] = [{
    name: "Sudoku Solver Website",
    description: "A website to solve sudoku problems. Solver uses generalized arc consistency to solve boards more efficiently. Built with react and hosted with Netlify.",
    skills: ["React", "Javascript", "HTML", "CSS", "Netlify", "AI"],
    link: "https://supersudokusolver.netlify.app/",
    img: sudokuImg
}, {
    name: "Anova Test Website",
    description: "A website to perform one-way and two-way anova tests. Built with react and hosted with Netlify.",
    skills: ["React", "Javascript", "HTML", "CSS", "Netlify", "Statistics"],
    link: "https://anovatest.netlify.app/",
    img: anovaImg
}]

</script>

<template>
    <ThemeDiv >
        <FadeInContainer>
            <div class="project-container">
                <h1>Projects</h1>
            </div>
            <div class="project-grid">
                <ProjectCard v-for="project in projects" :project="project"/>
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
        justify-content: center;
    }

    h1 {
        font-size: 3rem;
        font-weight: 200;
        text-align: center;
    }
</style>