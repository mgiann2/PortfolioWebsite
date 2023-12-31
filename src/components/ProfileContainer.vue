<script setup lang="ts">
import FadeInContainer from './FadeInContainer.vue';
import ThemeDiv from './ThemeDiv.vue';
import profilePhoto from '../assets/profile-photo.jpg';
</script>

<template>
    <ThemeDiv>
        <FadeInContainer>
            <div class="profile-container">
                <div class="picture-div">
                    <img class="profile-photo" :src="profilePhoto" alt="Profile Photo">
                </div>
                <div class="content-div">
                    <div style="height: 85%;">
                        <h1>Matteo Giannone</h1>
                        <h2 style="color: var(--dark-green);">Software Developer</h2>
                        <div class="paragraph-div">
                            <p>I'm a future 2024 University of Toronto graduate majoring in Computer Science and Applied Statistics. Over the course of my university career, I have worked on projects in many different fields of computer science. These include: Machine Learning, Artificial Intelligence, Fullstack Web Development, and Computer Security.</p>
                            <p>I am passionate about learning and creating new things. Recently, I've been interested in developing web apps and creating games with the open-source Godot game engine. Below are links to some of the projects I have worked on.</p>
                            <p>I am interested in any opportunities to hone my development skills and create amazing products!</p>
                        </div>
                    </div>
                    <div class="link-div">
                        <a href="https://www.linkedin.com/in/matteo-giannone/" target="_blank" class="link-icon">
                            <svg xmlns="http://www.w3.org/2000/svg" width="48" height="48" fill="currentColor" viewBox="0 0 16 16">
                                <path d="M0 1.146C0 .513.526 0 1.175 0h13.65C15.474 0 16 .513 16 1.146v13.708c0 .633-.526 1.146-1.175 1.146H1.175C.526 16 0 15.487 0 14.854V1.146zm4.943 12.248V6.169H2.542v7.225h2.401zm-1.2-8.212c.837 0 1.358-.554 1.358-1.248-.015-.709-.52-1.248-1.342-1.248-.822 0-1.359.54-1.359 1.248 0 .694.521 1.248 1.327 1.248h.016zm4.908 8.212V9.359c0-.216.016-.432.08-.586.173-.431.568-.878 1.232-.878.869 0 1.216.662 1.216 1.634v3.865h2.401V9.25c0-2.22-1.184-3.252-2.764-3.252-1.274 0-1.845.7-2.165 1.193v.025h-.016a5.54 5.54 0 0 1 .016-.025V6.169h-2.4c.03.678 0 7.225 0 7.225h2.4z"/>
                            </svg>
                        </a>
                        <a href="https://github.com/mgiann2" target="_blank" class="link-icon">
                            <svg xmlns="http://www.w3.org/2000/svg" width="48" height="48" fill="currentColor" viewBox="0 0 16 16">
                                <path d="M8 0C3.58 0 0 3.58 0 8c0 3.54 2.29 6.53 5.47 7.59.4.07.55-.17.55-.38 0-.19-.01-.82-.01-1.49-2.01.37-2.53-.49-2.69-.94-.09-.23-.48-.94-.82-1.13-.28-.15-.68-.52-.01-.53.63-.01 1.08.58 1.23.82.72 1.21 1.87.87 2.33.66.07-.52.28-.87.51-1.07-1.78-.2-3.64-.89-3.64-3.95 0-.87.31-1.59.82-2.15-.08-.2-.36-1.02.08-2.12 0 0 .67-.21 2.2.82.64-.18 1.32-.27 2-.27.68 0 1.36.09 2 .27 1.53-1.04 2.2-.82 2.2-.82.44 1.1.16 1.92.08 2.12.51.56.82 1.27.82 2.15 0 3.07-1.87 3.75-3.65 3.95.29.25.54.73.54 1.48 0 1.07-.01 1.93-.01 2.2 0 .21.15.46.55.38A8.012 8.012 0 0 0 16 8c0-4.42-3.58-8-8-8z"/>
                            </svg>
                        </a>
                    </div>
                </div>
            </div>
        </FadeInContainer>
    </ThemeDiv>
</template>

<style scoped>
    .profile-container {
        display: flex;
        height: calc(100vh - 12.8rem);
        margin: 1.5rem 10%;
    }

    .picture-div {
        aspect-ratio: 2/3;
        height: 100%;
        background-color: var(--light-green);
    }

    .profile-photo {
        width: 100%;
        height: 100%;
        border: solid 2px var(--light-green);
    }

    .content-div {
        display: flex;
        flex-direction: column;
        justify-content: space-between;
        position: relative;
        height: 100%;
        width: 100%;
        flex: 60%;
        padding: 0 1rem;
    }

    .paragraph-div {
        overflow-y: scroll;
        scrollbar-width: none;
        -ms-overflow-style: none;
        height: calc(100% - 7rem);
    }

    .paragraph-div::-webkit-scrollbar {
        display: none;  /* Safari and Chrome */
    }

    .link-div {
        display: flex;
        justify-content: right;
    }

    .link-icon {
        margin-right: 0.5rem;
        text-decoration: none;
        color: var(--light-green);
        transition: all 0.2s;
    }

    .link-icon:hover {
        transform: translateY(-0.2rem);
    }

    h1 {
        font-size: 3.25rem;
        margin: 0;
        font-weight: 200;
        color: var(--light-green);
    }

    h2 {
        font-size: 2.25rem;
        margin: 0;
        font-weight: 200;
        color: var(--white);
    }

    p {
        font-size: 1.5rem;
        margin: 0.8rem 0;
    }

    @media screen and (max-width: 900px) {
        .profile-container {   
            flex-direction: column-reverse;
            height: auto;
        }

        .picture-div {
            margin-top: 1rem;
            aspect-ratio: 9/13;
            height: 400px;
        }

        h1 {
            font-size: 3rem;
            margin: 0;
            font-weight: 200;
            color: var(--light-green);
        }

        h2 {
            font-size: 2rem;
            margin: 0;
            font-weight: 200;
            color: var(--white);
        }

        p {
            font-size: 0.95rem;
            line-height: 1.25rem;
            margin: 0.8rem 0;
        }

        .link-div {
            display: flex;
            justify-content: left;
        }
    }
</style>