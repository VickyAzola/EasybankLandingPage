<script setup>
import { ref } from 'vue'
import Logo from '/images/logo.svg'
import Hamburger from '/images/icon-hamburger.svg'
import Close from '/images/icon-close.svg'
import TheButton from './TheButton.vue'

let open = ref(false)

function menuOpen() {
    open.value = !open.value
}

const navLinks = [
    {id:0, text: 'Home'},
    {id:1, text: 'About'},
    {id:2, text: 'Contact'},
    {id:3, text: 'Blog'},
    {id:4, text: 'Careers'},
]

</script>

<template>
    <header class="nav-header">

        <div class="logo-and-icon">
            <a href="#">
                <img :src="Logo" alt="Logo Insure"/>
            </a>
            <button @click="menuOpen()">
                <img :src="[open ? Close : Hamburger]" alt="Open or Close menu mobile" />
            </button>
        </div>

        <nav 
            class="topNav" 
            @click="menuOpen()" 
            :class="[open ? 'block' : 'hidden']" 
            aria-label="Top Navigation"
            id="topNavigation"
        >
            <ul>
                <li v-for="link in navLinks">
                    <a href="#"> {{ link.text }} </a>
                </li>
            </ul>
        </nav>

        <div class="buttonDesktop">
            <TheButton text="Request Invite" />
        </div>

    </header>
</template>

<style scoped>
.nav-header {
    background-color: white;
    height: 4rem;
    padding-inline: 1rem;
    position: fixed;
    top: 0; 
    z-index: 3;
    width: 100%;
}

.logo-and-icon {
    height: 4rem;
    justify-content: space-between;
    display: flex;
    align-items: center;
}

.logo-and-icon button {
    position: absolute;
    z-index: 3;
    top: 0; 
    right: 0;
    padding: 1.5rem;
}

.topNav {
    background: linear-gradient(rgba(0, 0, 0, 0.651), rgba(0, 0, 0, 0.055));
    min-height: 90vh;
    width: 100%;
    position: absolute;
    left: 0;
    z-index: 3;
}

.topNav ul {
    background-color: white;
    width: 90%;
    padding: 1.5rem;
    min-height: min-content;
    position: absolute;
    margin-inline: auto;
    inset-inline: 0;
    z-index: 3;
    text-align: center;
    top: 2rem;
    border-radius: .3rem;
}

.topNav li {
    padding: .5rem 0;
}

.buttonDesktop {
    display: none;
}

@media screen and (min-width: 700px) {
    .nav-header {
        height: 4rem;
        padding-inline: 2rem;
        display: flex;
        justify-content: space-between;
    }

    .logo-and-icon {
        height: 4.5rem;
    }
    
    .logo-and-icon button {
        display: none;
    }
    
    .topNav {
        display: block;
        background: white;
        min-height: min-content;
        width: min-content;
        top: 1.2rem;
        inset-inline: 0;
        margin-inline: auto;
    }

    .topNav ul {
        position: static;
        background-color: white;
        display: flex;
        column-gap: 1rem;
        width: min-content;
        padding: 0;
        height: min-content;
        text-align: center;
        
    }

    .topNav li {
        padding: 0;
    }

    .topNav a {
        font-size: .8rem;
        padding: 1.35rem 0;
        color: var(--GrayishBlue);
    }

    .topNav li:hover a {
        color: var(--DarkBlue);
        border-bottom: 3px solid var(--LimeGreen);
    }

    .buttonDesktop {
        display: block;
    }
}

@media screen and (min-width: 1000px) {
    .nav-header {
        padding-inline: 4rem;
    }
    .topNav a {
        font-size: .9rem;
    }
}

@media screen and (min-width: 1440px) {
    .nav-header {
        padding-inline: 8rem;
    }

    .topNav a {
        font-size: 1rem;
    }

    .topNav ul {
        column-gap: 1.5rem;
    }
}
</style>
