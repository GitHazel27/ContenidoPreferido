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
        <h1>Catálogo</h1>
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
            <li :class="{activo: menuActivo === 'emprendimiento'}">
                <a href="#emprendimiento" class="nav-link" @click="setMenuActivo('emprendimiento')">
                <svg width="800px" height="800px" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
                <circle cx="12" cy="12" r="10" stroke="#000000" stroke-width="2"/>
                <path d="M15 9.94728C14.5 9.3 13.8 8.5 12 8.5C10.2 8.5 9 9.51393 9 9.94728C9 10.3806 9.06786 10.9277 10 11.5C10.7522 11.9618 12.6684 12.0439 13.5 12.5C14.679 13.1467 14.8497 13.8202 14.8497 14.0522C14.8497 14.6837 13.4175 15.4852 12 15.5C10.536 15.5153 9.5 14.7 9 14.0522" stroke="#000000" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/>
                <path d="M12 7V17" stroke="#000000" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"/>
                </svg>
                <div>
                    <h3>Emprendimiento</h3>
                </div>
            </a></li>
            <li><a href="#joyeria" class="nav-link">
                <svg fill="#000000" width="800px" height="800px" viewBox="0 0 50 50" version="1.2" baseProfile="tiny" xmlns="http://www.w3.org/2000/svg" overflow="inherit"><path d="M46.476 20.662l-.013-.101c-.028-.141-.08-.283-.127-.362l-6.336-10.199s-.808-1-1-1h-27l-8.12 10.853-.096.1-.013.047c-.064.101-.119.215-.168.35l-.033.097c-.048.166-.07.31-.064.526.007.14.032.279.077.424l.038.109c.051.129.114.247.188.352l19.631 24.867.04.057c.101.13.224.245.374.35l.114.071c.112.07.229.126.399.188l.111.037c.192.049.359.072.522.072.165 0 .326-.022.543-.078l.133-.047c.13-.046.247-.103.388-.19l.088-.055c.151-.107.272-.223.339-.314l19.656-24.893c.088-.114.162-.242.25-.469.048-.126.069-.248.08-.321l.015-.129.008-.102-.024-.24zm-10.54-.662l2.798-5.063 2.796 5.063h-5.594zm-1.678 3h6.638l-11.064 14.015 4.426-14.015zm-1.642-4.518l-4.041-5.482h7.07l-3.029 5.482zm-12.944 4.518h10.659l-5.331 16.877-5.328-16.877zm1.057-3l4.271-5.796 4.271 5.796h-8.542zm-3.008-1.972l-1.852-5.028h5.557l-3.705 5.028zm2.449 18.988l-11.065-14.016h6.639l4.426 14.016zm-7.505-22.044l1.853 5.028h-5.558l3.705-5.028z"/></svg>
                <div>
                    <h3>Joyeria</h3>
                </div>
            </a></li>
            <li><a href="#outfits" class="nav-link">
                <svg width="30px" height="30px" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
                <path fill-rule="evenodd" clip-rule="evenodd" d="M11.6597 5.75C10.8236 5.75 10.2857 6.34219 10.2857 6.90909C10.2857 7.3233 9.94987 7.65909 9.53566 7.65909C9.12145 7.65909 8.78566 7.3233 8.78566 6.90909C8.78566 5.36727 10.1497 4.25 11.6597 4.25C13.1697 4.25 14.5337 5.36727 14.5337 6.90909C14.5337 7.58928 14.2865 8.22354 13.8444 8.7044C13.7045 8.85669 13.5496 9.00942 13.4085 9.14851C13.3834 9.17327 13.3587 9.1976 13.3346 9.22141C13.1675 9.38672 13.0202 9.53616 12.8939 9.68456C12.8066 9.78721 12.7396 9.87796 12.6889 9.95888C13.2574 10.0668 13.8094 10.2856 14.3035 10.6187L21.736 15.629C22.6856 16.2692 22.9429 17.3256 22.6125 18.2165C22.2875 19.0928 21.4219 19.75 20.2973 19.75H3.70231C2.58964 19.75 1.72778 19.1049 1.39567 18.2392C1.05806 17.3591 1.29658 16.3086 2.22358 15.6566L9.31927 10.6653C9.85574 10.2879 10.4656 10.0483 11.093 9.94251C11.1984 9.43649 11.4859 9.02479 11.7513 8.71278C11.9231 8.51074 12.1111 8.32181 12.2797 8.15509C12.3074 8.12767 12.3345 8.10096 12.3609 8.07485C12.5028 7.93486 12.6272 7.81207 12.7402 7.68925C12.9223 7.49112 13.0337 7.22136 13.0337 6.90909C13.0337 6.34219 12.4958 5.75 11.6597 5.75ZM13.4651 11.8624C12.9825 11.5371 12.3993 11.373 11.81 11.3799C11.2256 11.3866 10.6525 11.5614 10.1823 11.8922L3.08659 16.8834C2.7415 17.1262 2.69597 17.4407 2.79616 17.7019C2.90185 17.9775 3.19965 18.25 3.70231 18.25H20.2973C20.8056 18.25 21.103 17.9729 21.2061 17.6949C21.3038 17.4314 21.2543 17.1133 20.8976 16.8728L13.4651 11.8624Z" fill="#171717" stroke="#171717" stroke-width=".5" stroke-linejoin="round"/>
                </svg>
                <div>
                    <h3>Outfits</h3>
                </div>
            </a></li>
            <li><a href="#seguidos" class="nav-link">
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
    gap: 5px;
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