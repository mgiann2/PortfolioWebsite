<script setup lang="ts">
import { ref, onMounted, onUnmounted } from 'vue';
import SpeedInContainer from './SpeedInContainer.vue';
import resume from '../assets/resume.pdf'

const screenSizeBreakpoint = 700;

const hideNav = ref(false);
const startY = ref();
const isSmallScreen = ref(false);
const hideSidebar = ref(true);

function toggleSidebar() {
    hideSidebar.value = !hideSidebar.value;
}

function handleScroll() {
    let scrollY = window.scrollY;
    if (scrollY > startY.value) {
        hideNav.value = true;
    } else {
        hideNav.value = false;
    }
    startY.value = scrollY;
}

function handleResize() {
    isSmallScreen.value = window.innerWidth < screenSizeBreakpoint;
}

onMounted(() => {
    window.addEventListener('scroll', handleScroll);
    window.addEventListener('resize', handleResize);
    handleResize();
});

onUnmounted(() => {
    window.removeEventListener('scroll', handleScroll);
    window.removeEventListener('resize', handleResize);
});

</script>

<template>
    <div class="navbar" :class="{'nav-hidden': hideNav}">
        <div class="nav-left">
            <SpeedInContainer>
                <svg width="80" height="55"
                    viewBox="0 0 21 14.599999"
                    version="1.1"
                    id="svg5"
                    inkscape:version="1.2.2 (732a01da63, 2022-12-09)"
                    sodipodi:docname="logo.svg"
                    xmlns:inkscape="http://www.inkscape.org/namespaces/inkscape"
                    xmlns:sodipodi="http://sodipodi.sourceforge.net/DTD/sodipodi-0.dtd"
                    xmlns="http://www.w3.org/2000/svg"
                    xmlns:svg="http://www.w3.org/2000/svg">
                    <sodipodi:namedview
                        id="namedview7"
                        pagecolor="#ffffff"
                        bordercolor="#000000"
                        borderopacity="0.25"
                        inkscape:showpageshadow="2"
                        inkscape:pageopacity="0.0"
                        inkscape:pagecheckerboard="0"
                        inkscape:deskcolor="#d1d1d1"
                        inkscape:document-units="px"
                        showgrid="false"
                        inkscape:zoom="5.5304152"
                        inkscape:cx="28.93092"
                        inkscape:cy="36.525287"
                        inkscape:window-width="1920"
                        inkscape:window-height="974"
                        inkscape:window-x="-11"
                        inkscape:window-y="-11"
                        inkscape:window-maximized="1"
                        inkscape:current-layer="layer1" />
                    <defs
                        id="defs2">
                        <inkscape:perspective
                        sodipodi:type="inkscape:persp3d"
                        inkscape:vp_x="0 : -133.9 : 1"
                        inkscape:vp_y="0 : 999.99995 : 0"
                        inkscape:vp_z="210 : -133.9 : 1"
                        inkscape:persp3d-origin="105 : -183.4 : 1"
                        id="perspective3205" />
                        <rect
                        x="101.25822"
                        y="235.787"
                        width="112.83059"
                        height="133.08223"
                        id="rect481" />
                        <rect
                        x="120.06332"
                        y="312.45392"
                        width="157.67351"
                        height="163.4597"
                        id="rect475" />
                    </defs>
                    <g
                        inkscape:label="Layer 1"
                        inkscape:groupmode="layer"
                        id="layer1"
                        transform="translate(-1.7411581,-2.8065388)">
                        <rect
                        style="fill:#42b0db;fill-opacity:1;stroke-width:0.0304606"
                        id="rect3318"
                        width="1"
                        height="3"
                        x="1.7411581"
                        y="2.8065388" />
                        <text
                        xml:space="preserve"
                        transform="scale(0.26458333)"
                        id="text473"
                        style="white-space:pre;shape-inside:url(#rect475);display:inline;fill:#000000" />
                        <text
                        xml:space="preserve"
                        transform="scale(0.26458333)"
                        id="text479"
                        style="white-space:pre;shape-inside:url(#rect481);display:inline;fill:#000000" />
                        <text
                        xml:space="preserve"
                        style="font-style:normal;font-variant:normal;font-weight:normal;font-stretch:normal;font-size:3.175px;font-family:'Berlin Sans FB Demi';-inkscape-font-specification:'Berlin Sans FB Demi';fill:#000000;stroke-width:0.264583"
                        x="62.385311"
                        y="104.10309"
                        id="text487"><tspan
                            sodipodi:role="line"
                            id="tspan485"
                            style="font-style:normal;font-variant:normal;font-weight:normal;font-stretch:normal;font-family:'Berlin Sans FB Demi';-inkscape-font-specification:'Berlin Sans FB Demi';stroke-width:0.264583"
                            x="62.385311"
                            y="104.10309" /></text>
                        <text
                        xml:space="preserve"
                        style="font-style:normal;font-variant:normal;font-weight:normal;font-stretch:normal;font-size:13.1866px;font-family:Bahnschrift;-inkscape-font-specification:Bahnschrift;fill:#000000;stroke-width:0.329666"
                        x="11.0351"
                        y="15.623242"
                        id="text545"
                        transform="scale(1.0616824,0.94190127)"><tspan
                            sodipodi:role="line"
                            id="tspan543"
                            style="font-style:normal;font-variant:normal;font-weight:normal;font-stretch:normal;font-family:Bahnschrift;-inkscape-font-specification:Bahnschrift;fill:#42b0db;fill-opacity:1;stroke-width:0.329666"
                            x="11.0351"
                            y="15.623242">G</tspan></text>
                        <text
                        xml:space="preserve"
                        style="font-style:normal;font-variant:normal;font-weight:normal;font-stretch:normal;font-size:12.1257px;font-family:'Berlin Sans FB';-inkscape-font-specification:'Berlin Sans FB';fill:#000000;stroke-width:0.303145"
                        x="4.9362974"
                        y="14.16299"
                        id="text541"
                        transform="scale(0.95653597,1.045439)"><tspan
                            sodipodi:role="line"
                            id="tspan539"
                            style="font-style:normal;font-variant:normal;font-weight:normal;font-stretch:normal;font-size:12.1257px;font-family:Bahnschrift;-inkscape-font-specification:Bahnschrift;fill:#57db6d;fill-opacity:1;stroke-width:0.303145"
                            x="4.9362974"
                            y="14.16299">M</tspan></text>
                        <rect
                        style="fill:#42b0db;fill-opacity:1;stroke-width:0.0393244"
                        id="rect3518"
                        width="1"
                        height="5"
                        x="-3.8065388"
                        y="1.7411581"
                        transform="rotate(-90)" />
                        <rect
                        style="fill:#57db6d;fill-opacity:1;stroke-width:0.0393243"
                        id="rect3520"
                        width="1"
                        height="5"
                        x="-17.406538"
                        y="17.741158"
                        transform="rotate(-90)" />
                        <rect
                        style="fill:#57db6d;fill-opacity:1;stroke-width:0.0304606"
                        id="rect3522"
                        width="1"
                        height="3"
                        x="-22.741158"
                        y="-17.406538"
                        transform="scale(-1)" />
                    </g>
                </svg>
            </SpeedInContainer>
        </div>
        <div class="nav-center">

        </div>
        <div class="nav-right">
            <SpeedInContainer v-if="!isSmallScreen">
                <slot />
                <a class="nav-btn" target="_blank" :href="resume">RESUME</a>
            </SpeedInContainer>
            <SpeedInContainer v-else>
                <div style="display: flex; justify-content: right; align-items: center;">
                    <a class="nav-btn" href="#">RESUME</a>
                    <div class="menu-btn" @click="toggleSidebar">
                        <div class="menu-bar"></div>
                        <div class="menu-bar"></div>
                        <div class="menu-bar"></div>
                    </div>
                </div>
            </SpeedInContainer>
        </div>
    </div>
    <div v-if="isSmallScreen" class="sidebar" :class="{'sidebar-hidden': hideSidebar}">
        <div class="close-btn" @click="toggleSidebar">
            <svg xmlns="http://www.w3.org/2000/svg" width="64" height="64" fill="currentColor" class="bi bi-x" viewBox="0 0 16 16">
                <path d="M4.646 4.646a.5.5 0 0 1 .708 0L8 7.293l2.646-2.647a.5.5 0 0 1 .708.708L8.707 8l2.647 2.646a.5.5 0 0 1-.708.708L8 8.707l-2.646 2.647a.5.5 0 0 1-.708-.708L7.293 8 4.646 5.354a.5.5 0 0 1 0-.708z"/>
            </svg>
        </div>
        <slot :click="toggleSidebar"/>
    </div>
</template>

<style scoped>
    .navbar {
        height: 3.8rem;
        position: sticky;
        top: 0;
        display: flex;
        align-items: center;
        justify-content: space-between;
        padding: 1rem;
        background-color: var(--black);
        z-index: 10;
        transition: transform 0.5s;
    }

    .nav-hidden {
        transform: translateY(-7rem);
    }

    .sidebar {
        position: fixed;
        left: 0;
        top: 0;
        width: 100%;
        height: 100%;
        background-color: var(--black);
        z-index: 90;
        display: flex;
        flex-direction: column;
        padding-top: 5rem;
        transition: all 0.5s ease-in-out;
    }

    .sidebar-hidden {
        transform: translate(800px);
    }

    .nav-left {
        display: flex;
        justify-content: left;
    }

    .nav-center {
        display: flex;
        justify-content: center;
    }

    .nav-right {
        display: flex;
        justify-content: right;
    }

    .nav-link {
        display: inline-block;
        padding: 1em;
        text-decoration: none;
        color: var(--red-orange);
    }

    .nav-btn {
        display: inline-block;
        margin-left: 2rem;
        padding: 1em;
        border-radius: 1em;
        border: solid var(--light-green) 2px;
        text-decoration: none;
        color: var(--light-green);
        transition: all 0.2s ease-in-out;
    }

    .nav-btn:hover {
        background-color: var(--light-green);
        color: var(--black);
    }

    .nav-btn:active {
        transform: scale(0.9);
    }

    .menu-btn {
        margin-left: 1rem;
        display: inline-block;
        cursor: pointer;
    }

    .menu-bar {
        width: 40px;
        height: 6px;
        background-color: var(--light-green);
        margin: 8px 0;
    }

    .close-btn {
        position: absolute;
        top: 0.9rem;
        right: 0.3rem;
        color: var(--light-green);
    }
</style>