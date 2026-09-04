<script setup lang="ts">
    import {ref} from 'vue'
    import emprendimiento1 from '../assets/imagenes/emprendimiento1.jpeg'
    import emprendimiento2 from '../assets/imagenes/emprendimiento2.jpeg'
    import joyeria1 from '../assets/imagenes/joyeria1.png'
    const contenidoE={
        idSeccion: 'emprendimiento',
        nombreSeccion: 'Emprendimiento',
        publicaciones:[
            {
                idPublicacion: 1,
                usuario: 'herprojectmx',
                fecha: '2026-08-27',
                titulo: 'Cómo usar ChatGPT para tu negocio',
                descripcion: 'Emprender también es aprender a usar herramientas que te faciliten el camino.',
                imagen: emprendimiento1,
                
            },
            {
                idPublicacion: 2,
                usuario: 'glowyourbiz.mx',
                fecha: '2026-02-01',
                titulo: '20 ganchos para vender más',
                descripcion: '¡Ya está aqui tu masterclass de la semana! Si no creces y vendes con tu contenido es porque no estás utilizando estos pasos.',
                imagen: emprendimiento2,
            }
        ]
    }

    function obtenerPublicaciones() {
  return contenidoE.publicaciones
}

const contenidoJ={
    idSeccion: 'joyeria',
    nombreSeccion: 'Joyeria',
    publicaciones:[
        {
            idPublicacion: 1,
            usuario: 'hazy_joyeria',
            fecha: '2025-08-27',
            titulo: 'Nuevos diseños de anillos dorados',
            descripcion: '✨ Descubre nuestra nueva colección de piezas doradas: flores oversize, motivos celestiales y acabados prémium resistentes al uso diario.',
            imagen: joyeria1,
            
        },
        {
            idPublicacion: 2,
            usuario: 'glowyourbiz.mx',
            fecha: '2026-02-01',
            titulo: '20 ganchos para vender más',
            descripcion: '¡Ya está aqui tu masterclass de la semana! Si no creces y vendes con tu contenido es porque no estás utilizando estos pasos.',
            imagen: 'https://via.placeholder.com/150',
        }
    ]
}

function obtenerPublicacionesJ() {
  return contenidoJ.publicaciones
}
</script>

<template>
<div>
    <section id="emprendimiento">
    <h2>{{ contenidoE.nombreSeccion }}</h2>
    <div class="publicaciones">
        <div class="publicacion" v-for="pub in obtenerPublicaciones()" :key="pub.idPublicacion">
            <h2>{{ pub.usuario }}</h2>
            <small>{{ pub.fecha }}</small>
            <h3>{{ pub.titulo }}</h3>
            <img :src="pub.imagen" :alt="pub.titulo">
            <p>{{ pub.descripcion }}</p>
            
        </div>
    </div>
    </section>
    <section id="joyeria">
        <h2>{{ contenidoJ.nombreSeccion }}</h2>
        <div class="publicaciones">
            <div class="publicacion" v-for="pub in obtenerPublicacionesJ()" :key="pub.idPublicacion">
                <h2>{{ pub.usuario }}</h2>
                <small>{{ pub.fecha }}</small>
                <h3>{{ pub.titulo }}</h3>
                <img :src="pub.imagen" :alt="pub.titulo">
                <p>{{ pub.descripcion }}</p>
            </div>
        </div>
    </section>
</div>
</template>

<style scoped>

section + section {
    border-top: 1px solid #dbdbdb;
    margin-top: 32px;
    padding-top: 24px;
}

h2 {
    font-family: instagram-font, sans-serif;
    color: #171717;
    margin-bottom: 20px;
}

small {
    font-family: instagram-font, sans-serif;
    color: #8e8e8e;
    margin-bottom: 10px;
}

p {
    font-family: instagram-font, sans-serif;
    color: #171717;
    margin-bottom: 10px;
}

h3 {
    font-family: instagram-font, sans-serif;
    color: #171717;
    margin-bottom: 10px;
    text-align: center;
}
.publicaciones {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
    gap: 20px;
}

.publicacion {
    background: #f9f2f5;
    border-radius: 12px;
    padding: 12px;
    box-shadow: 0 2px 8px rgba(0, 0, 0, 0.08);
}

.publicacion img {
    width: 65%;
    margin: 0 auto;
    aspect-ratio: 3.5 / 4;
    height: auto;
    object-fit: cover;
    border-radius: 8px;
    display: block;
}
</style>
