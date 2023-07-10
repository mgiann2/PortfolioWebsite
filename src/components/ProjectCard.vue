<script setup lang="ts">
import { type Project } from '../helper';

    defineProps<{
        project: Project
    }>();
</script>

<template>
    <div class="main-card">
        <div class="picture-div box-shadow">
            <img :src="project.img" alt="Image of a project">
        </div>
        <div class="content-div">
            <div style="height: 13rem; display: flex; flex-direction: column;">
                <h3>{{ project.name }}</h3>
                <p class="description">
                    {{ project.description }}
                </p>
                <div style="height: 100%; position: relative;">
                    <div class="skills">
                        <span v-for="skill in project.skills" class="skill-span">{{ skill }}</span>
                    </div>
                </div>
            </div>
            <a class="card-btn" target="_blank" :href="project.link">See Project</a>
        </div>
    </div>
</template>

<style scoped>
    .main-card {
        position: relative;
        background-color: #242424;
        display: flex;
        flex-direction: column;
        width: 18rem;
        border-radius: 1rem;
        transition: all 0.3s;
        border: solid 2px var(--black);
    }

    .main-card:hover {
        transform: translateY(-0.3rem);
        border-color: var(--light-green);
    }

    .picture-div {
        position: relative;
        height: 8rem;
    }

    .content-div {
        height: 16rem;
        padding: 1rem;
    }

    .card-btn {
        position: absolute;
        right: 1rem;
        bottom: 1rem;
        font-size: smaller;
        padding: 0.5rem;
        border-radius: 0.5rem;
        border: solid var(--light-green) 2px;
        text-decoration: none;
        color: var(--light-green);
        transition: all 0.2s ease-in-out;
    }

    .card-btn:hover {
        background-color: var(--light-green);
        color: var(--black);
    }

    .skills {
        position: absolute;
        bottom: 0;
        height: max-content;
        display: flex;
        flex-wrap: wrap;
        justify-content: left;
        gap: 0.3rem 0.5rem;
    }
    .skill-span {
        color: var(--red-orange);
    }

    h3 { 
        color: var(--light-green);
        margin: 0;
    }

    .box-shadow {
        position: relative;
        text-align: center;
    }

    .box-shadow::after {
        border-top-left-radius: 0.85rem;
        border-top-right-radius: 0.85rem;
        box-shadow: inset 0 0 6px #000000;
        bottom: 0;
        content: "";
        display: block;
        left: 0;
        height: 100%;
        position: absolute;
        right: 0;
        top: 0;
        width: 100%;
    }

    .box-shadow img {
        border-top-left-radius: 0.85rem;
        border-top-right-radius: 0.85rem;
        max-width: 100%;
        width: auto;
        height: 100%;
    }
</style>