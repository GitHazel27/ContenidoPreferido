<script setup lang="ts">
    import {ref} from 'vue'
    import emprendimiento1 from '../assets/imagenes/emprendimiento1.jpeg'
    import emprendimiento2 from '../assets/imagenes/emprendimiento2.jpeg'
    import emprendimiento3 from '../assets/imagenes/emprendimiento3.jpeg'
    import joyeria1 from '../assets/imagenes/joyeria1.png'
    import joyeria2 from '../assets/imagenes/joyeria2.png'
    import joyeria3 from '../assets/imagenes/joyeria3.png'
    import outfit3 from '../assets/imagenes/outfit3.jpeg'
    import hazy from '../assets/imagenes/hazy.png'
    import perfil1 from '../assets/imagenes/perfil1.jpeg'
    import perfil2 from '../assets/imagenes/perfil2.jpeg'
    import perfil3 from '../assets/imagenes/perfil3.jpeg'
    import perfil4 from '../assets/imagenes/perfil4.jpeg'
    import recom1 from '../assets/imagenes/recom1.jpeg'
    import recom2 from '../assets/imagenes/recom2.jpeg'
    import cat from '../assets/imagenes/cat.jpeg'
    import buuya from '../assets/imagenes/buuya.jpeg'

    const contenidoE={
        idSeccion: 'guardado',
        nombreSeccion: 'Guardado',
        descripcion:'Publiaciones que guardaste recientemente',
        publicaciones:[
            {
                idPublicacion: 1,
                perfil: perfil1,
                usuario: 'herprojectmx',
                titulo: 'Cómo usar ChatGPT para tu negocio',
                descripcion: 'Emprender también es aprender a usar herramientas que te faciliten el camino. ¿Qué consejo seguirías?',
                imagen: emprendimiento1,
                
            },
            {
                idPublicacion: 2,
                perfil: perfil2,
                usuario: 'glowyourbiz.mx',
                titulo: '20 ganchos para vender más',
                descripcion: '¡Ya está aqui tu masterclass de la semana! Si no creces y vendes con tu contenido es porque no estás utilizando estos pasos.',
                imagen: emprendimiento2,
            },
            {
            
                idPublicacion: 3,
                perfil: perfil3,
                usuario: 'diariodeunacreadora',
                titulo: '¿No tienes ideas para tu contenido?',
                descripcion: 'Si cada vez que entras a Tiktok piensas "¿y ahora qué publico?", este carrusel es para ti.',
                imagen: emprendimiento3,
            }
        ]
    }

    function obtenerPublicaciones() {
  return contenidoE.publicaciones
}

const contenidoJ={
    idSeccion: 'posts',
    nombreSeccion: 'Mis Posts',
    descripcion:'Tus publicaciones con más vistas',
    publicaciones:[
        {
            idPublicacion: 1,
            perfil: hazy,
            usuario: 'hazy_joyeria',
            titulo: 'Nuevos diseños de anillos dorados',
            descripcion: '✨ Descubre nuestra nueva colección de piezas doradas: flores oversize, motivos celestiales y acabados prémium resistentes al uso diario.',
            imagen: joyeria1,
            estrellas: 5,
            comentario:'',
            
        },
        {
            idPublicacion: 2,
            perfil: hazy,
            usuario: 'hazy_joyeria',
            titulo: 'Nuevos aretes ✨',
            descripcion: '¡Llegaron nuevos aretes! Diseños minimalistas y elegantes para cualquier ocasión. Ya puedes revisar el catálogo completo en la página web.',
            imagen: joyeria2,
            estrellas: 4,
            comentario:'',
        },
        {
            idPublicacion:3,
            perfil: hazy,
            usuario: 'hazy_joyeria',
            titulo: 'Relojes y brazaletes italianos',
            descripcion: 'Descubre nuestra selección de relojes y brazaletes italianos, perfectos para personalizar con charms.Revisa el catálogo.',
            imagen: joyeria3,
            estrellas: 5,
            comentario:'',
        }
    ]
}

function obtenerPublicacionesJ() {
  return contenidoJ.publicaciones
}

const contenidoO={
    idSeccion: 'recomendado',
    nombreSeccion: 'Recomendado',
    descripcion:'Publicaciones que podrían gustarte',
    publicaciones:[
        {
            idPublicacion: 1,
            perfil:cat,
            usuario: 'outfitlover',
            titulo: 'Outfit casual para el día a día',
            descripcion: 'Un look cómodo y estilizado para tus actividades diarias.',
            imagen: outfit3,
            
        },
        {
            idPublicacion: 2,
            perfil:buuya,
            usuario: 'buuya',
            titulo: 'Jewlery ✨🤍',
            descripcion: 'Combina prendas urbanas con accesorios modernos para un look único.',
            imagen: recom1,
        },
        {
        
            idPublicacion: 3,
            perfil:perfil4,
            usuario:'ella',
            titulo: 'Fotos para Instagram',
            descripcion: 'Es hora de tener fotos bonitas, recuerda mi frase INSTAGRAM NO ES TU CATÁLOGO.',
            imagen: recom2,
        }
    ]
}

function obtenerPublicacionesO() {
  return contenidoO.publicaciones
}
</script>

<template>
<div>
    <section id="posts">
        <h2>{{ contenidoJ.nombreSeccion }}</h2>
        <p>{{ contenidoJ.descripcion }}</p>
        <div class="publicaciones">
            <div class="publicacion" v-for="pub in obtenerPublicacionesJ()" :key="pub.idPublicacion">
                <div class="perfilF">
                    <img :src="pub.perfil" :alt="pub.usuario">
                </div>
                <h2>{{ pub.usuario }}</h2>
                <h3>{{ pub.titulo }}</h3>
                <div class="imagen">
                    <img :src="pub.imagen" :alt="pub.titulo">
                </div>
                <p>{{ pub.descripcion }}</p>
                <div class="estrellas" :aria-label="`${pub.estrellas} estrellas`">
                    <span v-for="estrella in pub.estrellas" :key="estrella">⭐</span>
                </div>
            </div>
        </div>
    </section>
        <section id="guardado">
    <h2>{{ contenidoE.nombreSeccion }}</h2>
    <p>{{ contenidoE.descripcion }}</p>
    <div class="publicaciones">
        <div class="publicacion" v-for="pub in obtenerPublicaciones()" :key="pub.idPublicacion">
            <div class="perfilF">
                    <img :src="pub.perfil" :alt="pub.usuario">
                </div>
            <h2>{{ pub.usuario }}</h2>
            <h3>{{ pub.titulo }}</h3>
            <div class="imagen">
                    <img :src="pub.imagen" :alt="pub.titulo">
            </div>
            <p>{{ pub.descripcion }}</p>
            
        </div>
    </div>
    </section>
    <section id="recomendado">
        <h2>{{ contenidoO.nombreSeccion }}</h2>
        <p>{{ contenidoO.descripcion }}</p>
        <div class="publicaciones">
            <div class="publicacion" v-for="pub in obtenerPublicacionesO()" :key="pub.idPublicacion">
                <div class="perfilF">
                    <img :src="pub.perfil" :alt="pub.usuario">
                </div>
                <h2>{{ pub.usuario }}</h2>
                <h3>{{ pub.titulo }}</h3>
                <div class="imagen">
                    <img :src="pub.imagen" :alt="pub.titulo">
                </div>
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
    margin-bottom: 10px;
    margin-top: 0%;
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
    grid-template-columns: repeat(3, minmax(0, 1fr));
    gap: 20px;
    align-items: center;
    text-align: center;
}

@media (max-width: 768px) {
    .publicaciones {
        grid-template-columns: repeat(2, minmax(0, 1fr));
    }
}

@media (max-width: 520px) {
    .publicaciones {
        grid-template-columns: 1fr;
    }
}

.publicacion {
    background: #f9f2f5;
    border-radius: 12px;
    padding: 12px;
    box-shadow: 0 2px 8px rgba(0, 0, 0, 0.08);
    height: auto;
    box-sizing: border-box;
    display: flex;
    flex-direction: column;
}

.imagen img {
    width: 65%;
    margin: 0 auto;
    aspect-ratio: 3.5 / 4;
    height: 280px;
    flex-shrink: 0;
    object-fit: cover;
    border-radius: 8px;
    display: block;
}

.perfilF img{
    border-radius: 50%;
    width: 60px;
    height: auto;
    margin-top: 10px;
    margin-bottom: 0%;
}

.publicacion p {
    width: 85%;
    margin: 15px auto 0px;
    overflow: hidden;
    display: -webkit-box;
    line-clamp: 4;
    -webkit-box-orient: vertical;
    -webkit-line-clamp: 4;
    
}

.estrellas {
    margin-top: 15px;
}
</style>
