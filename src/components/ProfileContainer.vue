<script setup lang="ts">
import FadeInContainer from './FadeInContainer.vue';
</script>

<template>
    <FadeInContainer>
        <div class="profile-container">
            <div class="picture-div">
            </div>
            <div class="content-div">
                <h1>Matteo Giannone</h1>
                <h2>Software Engineer</h2>
                <div class="footer-bar"></div>
            </div>
        </div>
    </FadeInContainer>
</template>

<style scoped>
    .profile-container {
        display: flex;
        height: calc(100vh - 8.8rem);
        margin: 1.5rem 10%;
    }

    .picture-div {
        height: 100%;
        width: 100%;
        background-color: var(--light-green);
        flex: 40%;
    }

    .content-div {
        position: relative;
        height: 100%;
        width: 100%;
        flex: 60%;
        padding: 0 1rem;
    }

    .footer-bar {
        position: absolute;
        bottom: 0;
        right: 0;
        width: 30%;
        height: 50px;
        border-bottom: solid 10px var(--light-green);
        border-right: solid 10px var(--light-green);
    }

    h1 {
        font-size: 3rem;
        margin: 0;
        margin-top: 0.5rem;
        font-weight: 200;
        color: var(--light-green);
    }

    h2 {
        font-size: 2rem;
        margin: 0;
        margin-top: 0.5rem;
        font-weight: 200;
        color: var(--white);
    }

    @media screen and (max-width: 900px) {
        .profile-container {   
            flex-direction: column;
        }
    }
</style>