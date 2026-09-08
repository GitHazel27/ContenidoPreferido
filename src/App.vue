<script setup lang="ts">
import Header from './components/Header.vue';
import ObjectoLiterals from './components/ObjectoLiterals.vue';
import foto1 from '../src/assets/imagenes/foto1.jpeg';
import foto2 from '../src/assets/imagenes/foto2.jpeg';
import foto3 from '../src/assets/imagenes/foto3.jpeg';
import foto4 from '../src/assets/imagenes/foto4.jpeg';
import hazy from '../src/assets/imagenes/hazy.png';

</script>

<template>
<Header></Header>

<main class="page-content">
  <section id="inicio">
    <div class="inicio">
      <div class="presentacion">
        <div class="perfil-emprendimiento">
          <div class="fotoP">
            <img :src="hazy" alt="Foto de perfil de Hazy joyería">
          </div>
          <h1 class="etiqueta">Hazy joyería</h1>
        </div>
        <h2>✨️Joyería de acero inoxidable✨️</h2>
        <p class="descripcion">
          Estamos los viernes en el tianguis de la Macroplaza<br>
          Entregas en FCA<br>
          📍Mérida, Yucatán<br>
          Consulta el catálogo👇
        </p>
        <a class="catalogo" href="https://canva.link/73nbf2gxj02cgtg" target="_blank" rel="noopener noreferrer">
          <svg fill="currentColor" version="1.1" id="Layer_1" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" 
	        width="30px" height="30px" viewBox="704.081 796 200 200" enable-background="new 704.081 796 200 200" xml:space="preserve">
          <path d="M891.876,977.909l-6.938-125.811h-34.661v-10.157c0-25.333-20.608-45.941-45.94-45.941s-45.94,20.609-45.94,45.941v10.157
	        h-36.161l-5.969,126.355l-0.006,0.219c-0.049,4.547,1.758,9.01,4.955,12.239c3.198,3.233,7.641,5.089,12.19,5.089h141.351
	        c4.688,0,9.228-1.953,12.453-5.36C890.434,987.233,892.135,982.593,891.876,977.909z M770.379,841.941
	        c0-18.725,15.233-33.959,33.958-33.959c18.724,0,33.958,15.234,33.958,33.959v10.157h-67.917V841.941z M878.507,982.402
	        c-0.973,1.026-2.339,1.615-3.751,1.615H733.405c-1.37,0-2.707-0.558-3.672-1.534c-0.942-0.95-1.483-2.257-1.492-3.597l5.423-114.806
	        h24.731v15.173c0,3.309,2.682,5.991,5.991,5.991c3.309,0,5.991-2.682,5.991-5.991v-15.173h67.917v15.173
	        c0,3.309,2.682,5.991,5.991,5.991c3.309,0,5.99-2.682,5.99-5.991v-15.173h23.321l6.313,114.49
	        C879.99,979.98,879.478,981.377,878.507,982.402z"/>
          </svg>
          <p>Catálogo</p>
        </a>
        <a class="enlace-social" href="https://www.tiktok.com/@hazy_joyeria?_r=1&_t=ZS-99ZIPpqt8dQ" target="_blank" rel="noopener noreferrer">
          <svg width="30px" height="30px" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg" aria-hidden="true"><path d="M20 7.50414C18.5333 7.56942 15.52 6.75998 15.2 3H12.4V13.9666C12.4 17.0999 9.93253 18.4412 8.289 17.2507C6.20169 15.7389 7.60003 12.5958 10.2 12.9874V9.6583C8.20003 9.6583 4 10.4416 4 15.3374C4 21.6041 10.8146 21.4083 12.4 20.5824C14.9798 19.2385 15.6 17.7827 15.6 14.5541C15.6 11.6166 15.6 9.85413 15.6 9.0708C16.2667 9.39719 18.08 10.0891 20 10.2458" stroke="currentColor" stroke-linecap="round" stroke-linejoin="round"/></svg>
          <p>@hazy_joyeria</p>
        </a>
      </div>
      <div class="galeria-fotos">
        
        <div class="espacio-foto">
          <img :src="foto1" alt="Foto del emprendimiento 1">
        </div>
        <div class="espacio-foto">
          <img :src="foto2" alt="Foto del emprendimiento 2">
        </div>
        <div class="espacio-foto">
          <img :src="foto3" alt="Foto del emprendimiento 3">
        </div>
        <div class="espacio-foto">
          <img :src="foto4" alt="Foto del emprendimiento 4">
        </div>
      </div>
    </div>
  </section>
  <ObjectoLiterals></ObjectoLiterals>
</main>
</template>

<style scoped>
.page-content {
  margin-left: 240px;
  padding: 24px;
}

section {
    border-bottom: 1px solid #dbdbdb;
    margin-bottom: 32px;
    padding-bottom: 24px;
}

.inicio {
  min-height: calc(100vh - 48px);
  max-width: 1100px;
  margin: 0 auto;
  display: grid;
  grid-template-columns: minmax(0, 1fr) minmax(280px, 420px);
  gap: clamp(32px, 7vw, 96px);
  align-items: center;
  padding: 48px 24px;
  box-sizing: border-box;
}

.presentacion {
  max-width: 580px;
}

.perfil-emprendimiento {
  display: flex;
  align-items: center;
  gap: 14px;
  margin-bottom: 20px;
}

.fotoP img {
  width: 64px;
  height: 64px;
  border-radius: 50%;
  object-fit: cover;
  display: block;
}

.etiqueta {
  margin: 0;
  color: #b43b70;
}

h1 {
  font-family: instagram-font, sans-serif;
  color: #171717;
  margin-bottom: 0px;
  margin-top: 0%;
  line-height: 0.98;
  font-size: 50px;
}

h2{
  font-family: instagram-font, sans-serif;
}

.descripcion {
  max-width: 500px;
  margin: 28px 0;
  color: #5d4c54;
  font-size: 1.1rem;
  line-height: 1.7;
  font-family: instagram-font, sans-serif;
}

.enlace-social {
  display: flex;
  align-items: center;
  gap: 8px;
  color: #171717;
  text-decoration: none;
  transition: color 0.2s ease, transform 0.2s ease;
  font-family: instagram-font, sans-serif;
}

.enlace-social p {
  margin: 0;
}

.enlace-social:hover {
  color: #d86b98;
  transform: translateY(-2px);
}

.enlace-social:hover svg {
  transform: scale(1.12);
}

.enlace-social svg {
  transition: transform 0.2s ease;
}

.galeria-fotos {
  display: grid;
  grid-template-columns: repeat(2, minmax(0, 1fr));
  gap: 14px;
}

.espacio-foto {
  aspect-ratio: 1;
  overflow: hidden;
  display: flex;
  justify-content: center;
  align-items: center;
  border: 4px  #d86b98;
  border-radius: 18px;
  background: #f9f2f5;
  color: #b43b70;
  font-size: 1.1rem;
  font-weight: 700;
}

.espacio-foto img {
  width: 100%;
  height: 100%;
  object-fit: cover;
  display: block;
}

@media (max-width: 760px) {
  .inicio {
    min-height: auto;
    grid-template-columns: 1fr;
    padding: 48px 12px 64px;
  }

  .galeria-fotos {
    max-width: 420px;
    margin: 0 auto;
  }
}

.catalogo {
  display: flex;
  align-items: center;
  gap: 8px;
  width: fit-content;
  margin-bottom: 10px;
  color: #171717;
  text-decoration: none;
  transition: color 0.2s ease, transform 0.2s ease;
  font-family: instagram-font, sans-serif;
}

.catalogo p {
  margin: 0;
}

.catalogo:hover {
  color: #d86b98;
  transform: translateY(-2px);
}

.catalogo:hover svg {
  transform: scale(1.12);
  color: #d86b98;
}

.catalogo svg {
  transition: transform 0.2s ease;
}
</style>
