<script setup lang="ts">
import { ref } from 'vue';
const menuActivo = ref('inicio');

const setMenuActivo = (menu: string) => {
  menuActivo.value = menu;
};
</script>

<template>
<header>
    <nav>
        <a href="#inicio">
            <h1>Mi perfil</h1>
        </a>
        <ul>
            <li :class="{activo: menuActivo === 'inicio'}">
                <a href="#inicio" class="nav-link" @click="setMenuActivo('inicio')">
                <svg width="30px" height="30px" viewBox="0 0 16 16" fill="none" xmlns="http://www.w3.org/2000/svg">
                <path d="M1 6V15H6V11C6 9.89543 6.89543 9 8 9C9.10457 9 10 9.89543 10 11V15H15V6L8 0L1 6Z" fill="#000000"/>
                </svg> 
                <div>
                    <h3>Inicio</h3>
                </div>
            </a></li>
            <li :class="{activo: menuActivo === 'posts'}">
                <a href="#posts" class="nav-link" @click="setMenuActivo('posts')">
                    <svg width="800px" height="800px" viewBox="0 0 16 16" xmlns="http://www.w3.org/2000/svg" fill="#000000" class="bi bi-grid-3x3-gap-fill">
                    <path d="M1 2a1 1 0 0 1 1-1h2a1 1 0 0 1 1 1v2a1 1 0 0 1-1 1H2a1 1 0 0 1-1-1V2zm5 0a1 1 0 0 1 1-1h2a1 1 0 0 1 1 1v2a1 1 0 0 1-1 1H7a1 1 0 0 1-1-1V2zm5 0a1 1 0 0 1 1-1h2a1 1 0 0 1 1 1v2a1 1 0 0 1-1 1h-2a1 1 0 0 1-1-1V2zM1 7a1 1 0 0 1 1-1h2a1 1 0 0 1 1 1v2a1 1 0 0 1-1 1H2a1 1 0 0 1-1-1V7zm5 0a1 1 0 0 1 1-1h2a1 1 0 0 1 1 1v2a1 1 0 0 1-1 1H7a1 1 0 0 1-1-1V7zm5 0a1 1 0 0 1 1-1h2a1 1 0 0 1 1 1v2a1 1 0 0 1-1 1h-2a1 1 0 0 1-1-1V7zM1 12a1 1 0 0 1 1-1h2a1 1 0 0 1 1 1v2a1 1 0 0 1-1 1H2a1 1 0 0 1-1-1v-2zm5 0a1 1 0 0 1 1-1h2a1 1 0 0 1 1 1v2a1 1 0 0 1-1 1H7a1 1 0 0 1-1-1v-2zm5 0a1 1 0 0 1 1-1h2a1 1 0 0 1 1 1v2a1 1 0 0 1-1 1h-2a1 1 0 0 1-1-1v-2z"/>
                    </svg>
                <div>
                    <h3>Mis Posts</h3>
                </div>
            </a></li>
            <li :class="{activo: menuActivo === 'guardado'}">
                <a href="#guardado" class="nav-link" @click="setMenuActivo('guardado')">
                <svg width="800px" height="800px" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
                <path d="M16.8203 2H7.18031C5.05031 2 3.32031 3.74 3.32031 5.86V19.95C3.32031 21.75 4.61031 22.51 6.19031 21.64L11.0703 18.93C11.5903 18.64 12.4303 18.64 12.9403 18.93L17.8203 21.64C19.4003 22.52 20.6903 21.76 20.6903 19.95V5.86C20.6803 3.74 18.9503 2 16.8203 2ZM15.0103 9.75C14.0403 10.1 13.0203 10.28 12.0003 10.28C10.9803 10.28 9.96031 10.1 8.99031 9.75C8.60031 9.61 8.40031 9.18 8.54031 8.79C8.69031 8.4 9.12031 8.2 9.51031 8.34C11.1203 8.92 12.8903 8.92 14.5003 8.34C14.8903 8.2 15.3203 8.4 15.4603 8.79C15.6003 9.18 15.4003 9.61 15.0103 9.75Z" fill="#171717"/>
                </svg>
                <div>
                    <h3>Guardado</h3>
                </div>
            </a></li>
            <li <li :class="{activo: menuActivo === 'recomendado'}">
                <a href="#recomendado" class="nav-link" @click="setMenuActivo('recomendado')">
                    <svg width="800px" height="800px" viewBox="0 0 24 24" version="1.1" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink">
                <!-- Uploaded to: SVG Repo, www.svgrepo.com, Generator: SVG Repo Mixer Tools -->
                <title>ic_fluent_checkmark_square_24_filled</title>
                <desc>Created with Sketch.</desc>
                <g id="🔍-System-Icons" stroke="none" stroke-width="1" fill="none" fill-rule="evenodd">
                <g id="ic_fluent_checkmark_square_24_filled" fill="#212121" fill-rule="nonzero">
                <path d="M18.7559,3 C19.9985,3 21.0059,4.00736 21.0059,5.25 L21.0059,5.25 L21.0059,18.75 C21.0059,19.9926 19.9985,21 18.7559,21 L18.7559,21 L5.25586,21 C4.01322,21 3.00586,19.9926 3.00586,18.75 L3.00586,18.75 L3.00586,5.25 C3.00586,4.00736 4.01322,3 5.25586,3 L5.25586,3 Z M15.2197,8.71966 L10.75,13.1891 L9.27654,11.7157 C8.98365,11.4228 8.50878,11.4228 8.21588,11.7157 C7.92299,12.0085 7.92299,12.4834 8.21589,12.7763 L10.2197,14.7801 C10.5126,15.073 10.9874,15.073 11.2803,14.7801 L16.2803,9.78034 C16.5732,9.48746 16.5732,9.01258 16.2804,8.71968 C15.9875,8.42678 15.5126,8.42677 15.2197,8.71966 Z" id="🎨-Color">

                </path>
                </g>
                </g>
                </svg>
                <div>
                    <h3>Recomendado</h3>
                </div>
            </a></li>
            <li :class="{activo: menuActivo === 'seguidos'}">
                <a href="#seguidos" class="nav-link" @click="setMenuActivo('seguidos')">
                <svg width="800px" height="800px" viewBox="0 0 16 16" xmlns="http://www.w3.org/2000/svg" fill="#000000" class="bi bi-people-fill">
                <path d="M7 14s-1 0-1-1 1-4 5-4 5 3 5 4-1 1-1 1H7zm4-6a3 3 0 1 0 0-6 3 3 0 0 0 0 6z"/>
                <path fill-rule="evenodd" d="M5.216 14A2.238 2.238 0 0 1 5 13c0-1.355.68-2.75 1.936-3.72A6.325 6.325 0 0 0 5 9c-4 0-5 3-5 4s1 1 1 1h4.216z"/>
                <path d="M4.5 8a2.5 2.5 0 1 0 0-5 2.5 2.5 0 0 0 0 5z"/>
                </svg>
                <div>
                    <h3>Seguidos</h3>
                </div>
            </a></li>
        </ul>
    </nav> 
</header>
</template>

<style scoped>

header{
    position: fixed;
    top: 0;
    left: 0;
    width: 240px;
    height: 100vh;
    z-index: 10;
}
.nav-link {
    display: flex;
    align-items: center;
    gap: 8px;
    text-decoration: none;
    color: inherit;
}

.nav-link svg {
  width: 30px;
  height: 30px;
  display: block;
  flex-shrink: 0;
}

.nav-link h3 {
    margin: 0;
    font-size: 17px;
    font-family: instagram-font, sans-serif;
    text-decoration: none;
}

h1 {
    font-family: instagram-font, sans-serif;
}

nav {
    background-color: #fceef5;
    border-right: 1px solid #dbdbdb;
    padding: 10px 20px;
    width: 100%;
    height: 100%;
    box-sizing: border-box;
}

nav ul {
    list-style: none;
    display: flex;
    flex-direction: column;
    gap: 15px;
    padding: 10px;
    margin: 0;
}

nav a {
    text-decoration: none;
    color: inherit;
}

nav a:hover {
    color: #000000;
}

nav li:hover {
    background-color: #ffc9d6;
    border-radius: 10px;
    padding: 5px;
    width: 100%;
}

nav li {
    display: flex;
    align-items: center;
    gap: 10px;
    padding: 5px;
}

nav li.activo {
    background-color: #ffc9d6;
    box-shadow: inset 0 0 0 1px #ffc9d6;
    border-radius: 10px;
    width: 100%;
}


</style>