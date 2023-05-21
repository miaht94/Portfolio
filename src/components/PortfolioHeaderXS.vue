<template>
<div class="header-xs-container">
    <img data-v-28e83e0a="" class="avatar" src="../assets/avt.jpg">
    <h1 class="name">Xuan-Bach Tran</h1>
    <h2 class="ocupation">Software Engineer</h2>
    <p class="current-location">Hanoi, Vietnam</p>
    <nav class="menu">
        <li>About me</li>
        <li>My Project</li>
    </nav>
    <div class="contact-icons">
        <div @click="coppyLinkedln()" @mouseleave="leaved()" class="icon">
            <svg width="25" height="25" viewBox="0 0 30 30" fill="none" xmlns="http://www.w3.org/2000/svg">
                <g clip-path="url(#clip0_310_2)">
                    <path d="M27.2863 0H2.71374C1.215 0 0 1.215 0 2.71374V27.2862C0 28.785 1.215 30 2.71374 30H27.2862C28.785 30 30 28.785 30 27.2862V2.71374C30 1.215 28.785 0 27.2863 0ZM9.28327 25.904C9.28327 26.3402 8.92971 26.6937 8.49353 26.6937H5.13181C4.69563 26.6937 4.34207 26.3402 4.34207 25.904V11.8118C4.34207 11.3756 4.69563 11.022 5.13181 11.022H8.49353C8.92971 11.022 9.28327 11.3756 9.28327 11.8118V25.904ZM6.81267 9.69361C5.04887 9.69361 3.61901 8.26374 3.61901 6.49995C3.61901 4.73615 5.04887 3.30628 6.81267 3.30628C8.57647 3.30628 10.0063 4.73615 10.0063 6.49995C10.0063 8.26374 8.57654 9.69361 6.81267 9.69361ZM26.8516 25.9676C26.8516 26.3686 26.5264 26.6937 26.1254 26.6937H22.5181C22.1171 26.6937 21.7919 26.3686 21.7919 25.9676V19.3575C21.7919 18.3715 22.0812 15.0365 19.215 15.0365C16.9918 15.0365 16.5408 17.3192 16.4503 18.3436V25.9676C16.4503 26.3686 16.1252 26.6937 15.7242 26.6937H12.2352C11.8342 26.6937 11.5091 26.3686 11.5091 25.9676V11.7481C11.5091 11.3471 11.8342 11.022 12.2352 11.022H15.7242C16.1252 11.022 16.4503 11.3471 16.4503 11.7481V12.9776C17.2747 11.7404 18.4998 10.7855 21.1083 10.7855C26.8846 10.7855 26.8516 16.1821 26.8516 19.1472V25.9676Z" 
                    fill="rgba(165, 164, 164, 0.93)"/>
                </g>
                <defs>
                    <clipPath id="clip0_310_2">
                        <rect width="30" height="30" fill="white"/>
                    </clipPath>
                </defs>
            </svg>
            <span> {{linkedinState ? "linkedin.com/in/miaht94" : "Coppied to your clipboard"}} </span>
        </div>
        <div @click="coppyGithub()" @mouseleave="leaved()" class="icon">
            <svg width="25" height="25" viewBox="0 0 25 25" fill="none" xmlns="http://www.w3.org/2000/svg">
                <path fill-rule="evenodd" clip-rule="evenodd" d="M12.5413 0C5.6018 0 0 5.73325 0 12.8356C0 18.4833 3.59518 23.2753 8.61172 24.9867C9.28059 25.0723 9.44781 24.73 9.44781 24.3877V22.1629C5.93623 22.933 5.18376 20.4514 5.18376 20.4514C4.59849 18.9967 3.7624 18.5689 3.7624 18.5689C2.59188 17.7987 3.84601 17.7987 3.84601 17.7987C5.10015 17.8843 5.76902 19.0823 5.76902 19.0823C6.85593 21.0504 8.69533 20.4514 9.44781 20.1092C9.53142 19.2535 9.86586 18.74 10.2839 18.3977C7.5248 18.0555 4.59849 16.943 4.59849 12.0655C4.59849 10.6964 5.10015 9.49837 5.85263 8.64266C5.68541 8.30038 5.26736 7.01681 5.93624 5.21982C5.93624 5.21982 7.02315 4.87754 9.3642 6.50339C10.3675 6.24668 11.4544 6.07553 12.5413 6.07553C13.6283 6.07553 14.7152 6.24668 15.7185 6.50339C18.1431 4.87754 19.1465 5.21982 19.1465 5.21982C19.8153 7.01681 19.3973 8.30038 19.2301 8.64266C20.0661 9.49837 20.4842 10.6964 20.4842 12.0655C20.4842 17.0286 17.5579 18.0555 14.7988 18.3977C15.2168 18.8256 15.6349 19.5957 15.6349 20.7937V24.3021C15.6349 24.6444 15.8857 25.0723 16.471 24.9011C21.4875 23.1897 24.9991 18.3977 24.9991 12.7501C25.0827 5.73325 19.4809 0 12.5413 0Z" 
                fill="rgba(165, 164, 164, 0.93)"/>
            </svg>
            <span>{{githubState ? "https://github.com/miaht94" : "Coppied to your clipboard"}} </span>
        </div>
        <div @click="coppyEmail()" @mouseleave="leaved()" class="icon">
            <svg width="25" height="18" viewBox="0 0 25 18" fill="none" xmlns="http://www.w3.org/2000/svg">
                <path d="M25 4.86V15.75C25 16.3467 24.7366 16.919 24.2678 17.341C23.7989 17.7629 23.163 18 22.5 18H2.5C1.83696 18 1.20107 17.7629 0.732233 17.341C0.263392 16.919 0 16.3467 0 15.75V5.27625L2.5 6.5025L11.9 11.115C12.0843 11.2045 12.2906 11.2509 12.5 11.25C12.7201 11.2479 12.9357 11.1936 13.125 11.0925L22.5 6.17625L25 4.86Z" fill="rgba(165, 164, 164, 0.93)"/>
                <path d="M25 2.25L22.5 3.5775L12.5 8.83125L2.5 3.9375L0 2.7V2.25C0 1.65326 0.263392 1.08097 0.732233 0.65901C1.20107 0.237053 1.83696 0 2.5 0H22.5C23.163 0 23.7989 0.237053 24.2678 0.65901C24.7366 1.08097 25 1.65326 25 2.25Z" fill="rgba(165, 164, 164, 0.93)"/>
            </svg>
            <span>{{emailState ? "tranxuanbach1@gmail.com" : "Coppied to your clipboard"}}</span>
        </div>
        <!-- <div></div> -->
    </div>
</div>  
</template>

<script setup>
import { ref } from 'vue';
const emailState = ref(true)
const githubState = ref(true)
const linkedinState = ref(true)
async function coppyEmail() {
    await copyToClipboard("tranxuanbach1@gmail.com")
    emailState.value = false
}

async function coppyGithub() {
    await copyToClipboard("https://github.com/miaht94")
    githubState.value = false
}

async function coppyLinkedln() {
    await copyToClipboard("https://linkedin.com/in/miaht94")
    linkedinState.value = false
}

async function copyToClipboard(textToCopy) {
    // Navigator clipboard api needs a secure context (https)
    if (navigator.clipboard && window.isSecureContext) {
        await navigator.clipboard.writeText(textToCopy);
    } else {
        // Use the 'out of viewport hidden text area' trick
        const textArea = document.createElement("textarea");
        textArea.value = textToCopy;
            
        // Move textarea out of the viewport so it's not visible
        textArea.style.position = "absolute";
        textArea.style.left = "-999999px";
            
        document.body.prepend(textArea);
        textArea.select();

        try {
            document.execCommand('copy');
        } catch (error) {
            console.error(error);
        } finally {
            textArea.remove();
        }
    }
}

function leaved() {
    linkedinState.value = true
    githubState.value = true
    emailState.value = true
}
</script>

<style scoped>

.header-xs-container {
    display: flex;
    flex-direction: column;
    width: 100%;
    height: 100%;
    
}

h1 {
    /* text-align: center; */
    font-size: 1.7rem;
    color: white;
    margin: 0;
}
h2 {
    /* text-align: center; */
    font-size: 1.4rem;
    color: rgb(255, 255, 255);
    margin: 0;
    font-weight: 400;
}

.avatar {
    margin-top: 20px;
    width: 100px;
    border-radius: 14px;
    align-self: center;
    /* margin-left: 30px */
}

.name {
    margin-top: 20px;
    padding-left: 30px
}

.ocupation {
    margin-top: 10px;
    padding-left: 30px
}

.current-location {
    font-size: 1.2rem;
    font-weight: 400;
    color: rgba(255, 255, 255, 0.675);
    margin-top: 5px;
    padding-left: 30px
}

.menu {
    margin-top: 10px;
    color: white;
    
}

.contact-icons {
    display: flex;
    padding-left: 30px;
    padding-right: 30px;
    flex-direction: column;
}


.icon {
    position: relative;
    padding-left: 5px;
    display: flex;
    flex-direction: row;
    align-items: center;
    margin-top: 20px;
    height: 40px;
    border: 1px solid white;
    border-radius: 6px;
    color: rgba(255, 255, 255, 0.766);
    font-family: 'Inter', sans-serif;
    font-weight: 600;
    font-size: 0.9rem;
    cursor: pointer;
}

.icon > svg {
    margin-right: 10px
}

.icon > * {
    z-index: 2;
}

.icon::after {
    content: "";
    z-index: 1;
    position: absolute;
    background-color: white;
    top: 0px;
    width: 0;
    height: 100%;
    right: 0px;
    border-radius: 6px;
    transition: 300ms ease-in-out
}

.icon:hover {
    transition: 300ms ease-in-out;
    color: rgba(0, 0, 0, 0.766)
}

.icon:hover::after {
    background-color: white;
    width: 100%;
}

li {
    position: relative;
    list-style-type: none;
    font-size: 1.2rem;
    /* color: rgba(255, 255, 255, 0.523); */
    line-height: 40px;
    padding-left: 30px;
    cursor: pointer;
}


li:hover::after {
    display: block;
    position: absolute;
    content: "";
    top: 0px;
    left: 10px;
    width: calc(100% - 20px);
    height: 100%;
    background-color: rgba(255, 255, 255, 0.27);
    border-radius: 10px;
}


li:active::after {
    display: block;
    position: absolute;
    content: "";
    top: 0px;
    left: 10px;
    width: calc(100% - 20px);
    height: 100%;
    background-color: rgba(255, 255, 255, 0.678);
    border-radius: 10px;
}

li.active::after {
    display: block;
    position: absolute;
    content: "";
    top: 0px;
    left: 10px;
    width: calc(100% - 20px);
    height: 100%;
    background-color: rgba(255, 255, 255, 0.678);
    border-radius: 10px;
}

/* li + li {
    margin-top: 10px
} */
</style>