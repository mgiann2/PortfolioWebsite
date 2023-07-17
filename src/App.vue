<script setup lang="ts">
import Navbar from './components/Navbar.vue';
import ProfileContainer from './components/ProfileContainer.vue';
import SkillsContainer from './components/SkillsContainer.vue';
import ProjectsContainer from './components/ProjectsContainer.vue';
import ContactContainer from './components/ContactContainer.vue';
</script>

<template>
    <Navbar>
        <a class="nav-link" href="#">About</a>
        <a class="nav-link" href="#skills">Skills</a>
        <a class="nav-link" href="#projects">Projects</a>
        <a class="nav-link" href="#get-in-touch">Get In Touch</a>
    </Navbar>
    <ProfileContainer />
    <SkillsContainer id="skills"/>
    <ProjectsContainer id="projects"/>
    <ContactContainer id="get-in-touch"/>
</template>

<style scoped>
    .nav-link {
        display: inline-block;
        padding: 1em;
        text-decoration: none;
        color: var(--red-orange);
        border: 2px solid var(--black);
        transition: all 0.2s;
    }

    .nav-link:hover {
        color: rgb(190, 96, 68);
        border-bottom-color: var(--red-orange);
    }
</style>
