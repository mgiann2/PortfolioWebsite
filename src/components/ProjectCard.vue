<script setup lang="ts">
    // defineProps<{
    //     img: string
    //     name: string
    //     description: string
    //     skills: string[]
    // }>();
</script>

<template>
    <div class="main-card">
        <div class="picture-div">
            <img src="" alt="">
        </div>
        <div class="content-div">
            <div style="height: 14rem;">
                <h3>Name</h3>
                <p class="description">
                    Lorem ipsum dolor sit amet, consectetur adipisicing elit. Veniam quod ad, veritatis doloremque, repudiandae accusamus perspiciatis perferendis explicabo, fugiat ullam sit maiores nihil! Modi ut autem, accusantium molestiae possimus atque?
                </p>
                <p class="skills">
                    <span class="skill-span">React</span>
                    <span class="skill-span">Javascript</span>
                </p>
            </div>
            <a class="card-btn" href="#">See Project</a>
        </div>
    </div>
</template>

<style scoped>
    .main-card {
        position: relative;
        background-color: var(--black);
        display: flex;
        flex-direction: column;
        width: 18rem;
        box-shadow: 0px 0px 5px 1px rgba(100, 100, 100, 0.5);
    }

    .picture-div {
        height: 8rem;
        background-color: var(--light-green);
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

    .skill-span {
        margin-right: 1rem;
        color: var(--red-orange);
    }

    p {
        font-size: smaller;
    }

    h3 { 
        color: var(--light-green);
        margin: 0;
    }

    img {
        width: 100%;
        height: 100%;
        object-fit: fill;
    }
</style>