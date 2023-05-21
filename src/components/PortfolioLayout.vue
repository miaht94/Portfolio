<template>
    <div class="layout-container">
        <header class="page-header">
            <a>Trần Xuân Bách</a>
            <div class="page-header__more-button-container" :class="{openning: menuOpenningState}">
                <svg @click="openMenu" class="page-header__more-button" fill="none" xmlns="http://www.w3.org/2000/svg">
                    <path class="more-button__bar-one" d="M17.3121 2H0.669974C0.294789 2 0 1.56291 0 0.993378C0 0.437087 0.294789 0 0.669974 0H17.3121C17.6873 0 18 0.437087 18 0.993378C18 1.56291 17.6873 2 17.3121 2Z" fill="white"/>
                    <path class="more-button__bar-second" d="M17.3121 8H0.669974C0.294789 8 0 7.56291 0 6.99338C0 6.43708 0.294789 6 0.669974 6H17.3121C17.6873 6 18 6.43708 18 6.99338C18 7.56291 17.6873 8 17.3121 8Z" fill="white"/>
                    <path class="more-button__bar-third" d="M17.3121 14H0.669974C0.294789 14 0 13.5496 0 12.9934C0 12.4372 0.294789 12 0.669974 12H17.3121C17.6873 12 18 12.4372 18 12.9934C18 13.5496 17.6873 14 17.3121 14Z" fill="white"/>
                </svg>
            </div>
            <nav class="page-navigator" :class="{openning : menuOpenningState}">
                <li class="nav-item">About me</li>
                <li class="nav-item">My project</li>
                <li class="nav-item">Contact</li>
            </nav>
        </header>
        <div class="page-header-xs">
            <PortfolioHeaderXS></PortfolioHeaderXS>
        </div>
        <div class="page-body"> 
            <PortfolioBody></PortfolioBody>
        </div>
        <footer></footer>
    </div>
</template>
<script setup>
import { ref } from "vue";
import PortfolioBody from "./PortfolioBody.vue";
import PortfolioHeaderXS from "./PortfolioHeaderXS.vue";
const menuOpenningState = ref(false)
function openMenu(event) {
    event.stopPropagation();
    event.currentTarget.classList.toggle("openning")
    menuOpenningState.value = !menuOpenningState.value
}

</script>
<style scoped>

li {
    list-style-type: none;
}

.layout-container {
    display: flex;
    flex-direction: column;
}


.page-header {
    position: sticky;
    text-align: center;
    display: flex;
    /* line-height: 20px; */
    font-family: 'Playfair Display', sans-serif;
    font-size: 1.25rem;
    color: white;
    font-weight: 900 !important;
    background-color: rgb(36, 36, 36);
    height: 60px;
    border-radius: 16px;
    top: 0px;
    z-index: 3;
}

.page-header-xs {
    display: none;
}

.page-header > a {
    margin: auto 20px auto
}

.page-header__more-button-container {
    display: flex;
    margin: auto 20px auto auto;
    width: 28px;
    height: 25px;
    border-radius: 3px;
    align-items: center;
    justify-content: center;
}

.page-header__more-button-container.openning {
    background-color: rgba(166, 169, 172, 0.144);
}
.page-header__more-button {
    width: 18px; 
    height: 15px;
}

.more-button__bar-one {
    transition: 200ms ease-in;
}

.more-button__bar-second {
    transition: 200ms ease-in;
}
.more-button__bar-third {
    transition: 200ms ease-in;
}

.page-header__more-button.openning > .more-button__bar-one {
    transform: rotate(40deg) translate(1px);
    transform-origin: 0.669974px 1px;
    transition: 200ms ease-in;
}

.page-header__more-button.openning > .more-button__bar-second {
    opacity: 0;
    transition: 200ms ease-in;
}
.page-header__more-button.openning > .more-button__bar-third {
    transform: rotate(-40deg) translate(1px);
    transform-origin: 0.669974px 13px;
    transition: 200ms ease-in;
}

.page-navigator {
    z-index: 3;
    opacity: 0;
    position: absolute;
    background-color: rgb(36, 36, 36);
    width: 100%;
    top: 100%;
    border-radius: 16px;
    transform: translate(0px, 5px);
    font-size: 1rem;
    transition: 200ms ease-in;
}

.page-navigator.openning {
    transition: 200ms ease-in;
    transform: translate(0px, 1px);
    opacity: 1;
}

.page-navigator > .nav-item {
    height: 30px;
    text-align: center;
    line-height: 30px;
    font-weight: 600;
}

.nav-item:first-of-type {
    border-radius: 16px 16px 0px 0px;
}

.nav-item:last-of-type {
    border-radius: 0px 0px 16px 16px;
}

.page-navigator > .nav-item:hover {
    background-color: rgba(143, 143, 143, 0.389);
    /* color: black */
}

.page-body {
    height: 1000px;
    display: flex;
    flex-direction: row;
}

@media screen and (min-width: 820px) {
    .page-header {
        display: none;
    }

    .page-body {
        margin-left: 320px
    }

    .page-header-xs {
        display: block;
        position: fixed;
        left: 10px;
        top: 4%;
        width: 300px;
        height: calc(100vh - 8%);
        background: #252525;
        border-radius: 16px;
    }
}
</style>