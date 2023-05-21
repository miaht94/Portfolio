<template>
 <div class="body-container">
    <div class="hello-section">
        <div class="heading">
            <h1 >👋 Hi! I'm Xuan-Bach Tran </h1>
            <h2>I'm trying to <span class="raiden-shogun" @mousemove="showRaidenShogun" @mouseout="hideRaidenShogun" style="color:rgba(173, 52, 243, 0.814)">Unleash</span> the Power of Code!</h2>
        </div>
        <img class="avatar-xs" src="https://media.tenor.com/2roX3uxz_68AAAAM/cat-space.gif"/>
    </div>
    
    <p>I am a final year student of University of Engineering and Technology - Vietnam National University (UET-VNU Vietnam) with a strong foundation in software development, combined with a deep love for problem-solving and innovation, I am dedicated to creating efficient and robust solutions that drive impactful results.</p>
    <img 
    :style="{'top': raidenShogunUnleashPosY + 40 + 'px', 'left': raidenShogunUnleashPosX + 'px'}"
    :hidden="!showRaidenShogunUnleash" 
    class="raiden-shogun-unleash" src="https://media.tenor.com/RI1uo-UzpNAAAAAC/genshin-impact-raiden-shogun.gif" width="833" height="468.3534136546185" alt="Genshin Impact Raiden Shogun GIF - Genshin Impact Raiden Shogun Baal GIFs"/>
    <div class="project-section">
        <h1>My Lastest Project</h1>
        <div class="project-grid" >
            <div class="tetris-project" @click="openInNewTab('https://github.com/miaht94/AppleMusic')">
                <img src="../assets/apple-music.png" alt="apple muvic">
                <div class="tetris-project__desc">
                    <span>A clone version of Apple Music on Android with Flutter </span>
                </div>
            </div>
            <div class="tetris-project" @click="openInNewTab('https://bitnews.world')">
                <img src="../assets/bitnews.png" alt="apple muvic">
                <div class="tetris-project__desc">
                    <span>A news aggregation system about cryptocurrency, deployed on Google Kubernetes Engine with CI/CD pipeline using ArgoCD and Github Action </span>
                </div>
            </div>
            <div class="tetris-project" @click="openInNewTab('https://github.com/miaht94/Tetris_SDL')">
                <img src="../assets/tetris.png" alt="apple muvic">
                <div class="tetris-project__desc">
                    <span>Tetris game on Windows (a clone version of tetris.com with many graphic effects) using SDL2 library</span>
                </div>
            </div>
            <div class="tetris-project" @click="openInNewTab('https://github.com/miaht94/Student-Management')">
                <img src="../assets/student-management.png" alt="apple muvic">
                <div class="tetris-project__desc">
                    <span>A site for university advisor can manage their student that they have responsibility in various aspects (score, tuition, training points, ...)</span>
                </div>
            </div>
            <div class="tetris-project" @click="openInNewTab('https://github.com/miaht94/Dictionary')">
                <img src="../assets/dictionary.png" alt="apple muvic">
                <div class="tetris-project__desc">
                    <span>A project with my friend for my OOP course at university using JavaFX. We leaked Apple Dictionary's Database and developed some fun features.</span>
                </div>
            </div>
        </div>
    </div>
 </div>
</template>

<script setup>
import { ref } from 'vue';
const raidenShogunUnleashPosX = ref(0)
const raidenShogunUnleashPosY = ref(0)
const showRaidenShogunUnleash = ref(false)
function showRaidenShogun(event) {
    console.log(event.clientX)
    showRaidenShogunUnleash.value = true
    raidenShogunUnleashPosX.value = event.clientX
    raidenShogunUnleashPosY.value = event.clientY
}

function hideRaidenShogun() {
    showRaidenShogunUnleash.value = false
}

function openInNewTab(url) {
  window.open(url, '_blank').focus();
}

</script>

<style scoped>

.body-container {
    padding-left: 10px;
    padding-right: 40px;
    margin-top: 30px;
    font-family: 'Playfair Display', sans-serif;
    /* width: 100vw; */
}

.body-container > h1 {
    font-weight: 900;
    font-size: 2.5rem;
    color: #252525
}

.body-container >>> p {
    font-family: Inter, sans-serif;
    color: #4f4f4f;
    font-size: 1.1rem;
}

.hello-section {
    display: flex;
    flex-direction: row;
    /* justify-content: center; */
    
}

.heading {
    flex-grow: 1;
}

.avatar-xs {
    width: 100px;
    height: 100px;
    /* right: 40px */
    align-self: center;
    border-radius: 16px;

}

.raiden-shogun {
    cursor: pointer;
    text-decoration: underline;
}


.raiden-shogun-unleash {
    z-index: 2;
    position: fixed;
    width: 400px;
    height: auto;
    border-radius: 10px;
}

.project-section {
    margin-top: 40px;
}

.project-grid {
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    grid-template-rows: repeat(3,300px);
    grid-column-gap: 40px;
    grid-row-gap: 20px;
}

.tetris-project {
    z-index: 1;
    position: relative;
    border-radius: 16px;
    overflow: hidden;
    margin-bottom: 10px;
    cursor: pointer;
}

.tetris-project img {
    object-fit: cover;
    width: 100%;
    height: 100%;
    border-radius: 16px;
    transition: 100ms ease-in;
}

.tetris-project__desc {
    display: flex;
    justify-content: center;
    padding: 10px;
    color: rgba(242, 242, 242, 0.974);
    font-family: 'Inter', sans-serif;
    font-weight: 300 !important;
    font-size: 0.9rem;
    position: absolute;
    bottom: 0px;
    left: 0px;
    height: 20%;
    width: 100%;
    background: rgba(90, 90, 90, 0.615);
    /* border-radius: 0px 0px; */
    box-shadow: 0 4px 30px rgba(0, 0, 0, 0.1);
    backdrop-filter: blur(5px);
    -webkit-backdrop-filter: blur(5.2px);
    transition: 100ms ease-in;
}

.tetris-project__desc span {
    justify-self: center;
    align-self: center;
}

.tetris-project:hover .tetris-project__desc {
    transition: 100ms ease-in;
    background: rgba(90, 90, 90, 0.786);
}

.tetris-project:hover img {
    transition: 100ms ease-in;
    transform-origin: 50% 50%;
    transform: scale(1.05);
}

h1 {
    font-weight: 900;
}

h2 {
    font-family: Inter, sans-serif;
    font-weight: 600;
    font-size: 1.5rem;
}

@media screen and (max-width: 479px) {
    .body-container > h1 {
        font-weight: 900;
        font-size: 2.2rem;
        line-height: 3rem;
        color: #252525
    }
    h2 {
        font-size: 1.2rem;
    }
    .avatar-xs {
        display: none;
    }

    .raiden-shogun-unleash {
        width: 200px;
        height: auto;
    }

    .tetris-project__desc {
        font-size: 0.8rem;
    }
}

@media screen and (min-width: 820px) {
    .body-container{
        margin-top: 10px;
    }
}

@media screen and (max-width: 960px) {
    .project-grid {
        display: grid;
        grid-template-columns: repeat(1, 1fr);
        grid-template-rows: repeat(5, 300px);
        grid-column-gap: 40px;
        grid-row-gap: 20px;
    }
}
</style>