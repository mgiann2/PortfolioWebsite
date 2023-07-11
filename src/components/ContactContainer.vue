<script setup lang="ts">
import ThemeDiv from './ThemeDiv.vue';
import FadeInContainer from './FadeInContainer.vue';
</script>

<template>
    <ThemeDiv main-color="var(--red-orange)" accent-color="var(--black)">
        <FadeInContainer style="color: var(--black)">
            <h1>Get In Touch</h1>
            <p>I'm currently finishing my university degree, however I'm always open to discuss any potential opportunities. My inbox is always open so feel free to shoot me a message! I'll try to get back to you as soon as possible.</p>
            <div style="display: flex; justify-content: center;">
                <abbr title="Get In Touch">
                    <a class="contact-btn" href="mailto:matteogiannone24@gmail.com" rel="noopener noreferrer">
                        <svg xmlns="http://www.w3.org/2000/svg" width="32" height="32" fill="currentColor" class="bi bi-envelope-fill" viewBox="0 0 16 16">
                            <path d="M.05 3.555A2 2 0 0 1 2 2h12a2 2 0 0 1 1.95 1.555L8 8.414.05 3.555ZM0 4.697v7.104l5.803-3.558L0 4.697ZM6.761 8.83l-6.57 4.027A2 2 0 0 0 2 14h12a2 2 0 0 0 1.808-1.144l-6.57-4.027L8 9.586l-1.239-.757Zm3.436-.586L16 11.801V4.697l-5.803 3.546Z"/>
                        </svg>
                    </a>
                </abbr>
            </div>
        </FadeInContainer>
    </ThemeDiv>
</template>

<style scoped>
    h1 {
        font-size: 3rem;
        font-weight: 200;
        text-align: center;
    }

    .contact-btn {
        display: flex;
        align-items: center;
        justify-content: center;
        margin: 1rem 0;
        padding: 0.75rem 1.75rem;
        border-radius: 1rem;
        border: solid var(--black) 2px;
        text-decoration: none;
        color: var(--red-orange);
        background-color: var(--black);
        transition: all 0.2s ease-in-out;
    }

    .contact-btn:hover {
        transform: scale(1.05);
    }

    p {
        margin: 16px 25%;
        text-align: center;
    }
</style>