---
name: imagen-de-perfil
description: "Coloca y valida imagenes de perfil en componentes Vue con TypeScript. Usar cuando una tarjeta, publicacion o usuario necesite un avatar o imagen de perfil local, incluyendo importacion de assets, datos reactivos, template, estilos y validacion."
argument-hint: "Indica el componente Vue y el archivo de imagen que debe usar el perfil"
user-invocable: true
---

# Imagen de perfil en Vue

## Cuando usar

- Agregar un avatar a tarjetas de publicaciones o perfiles.
- Reemplazar URLs placeholder por imagenes locales del proyecto.
- Corregir imagenes de perfil que no aparecen o no tienen texto alternativo.

## Procedimiento

1. Identifica el componente Vue que renderiza la tarjeta o publicacion y localiza el objeto de datos que representa cada usuario.
2. Comprueba que el archivo de imagen exista dentro de `src/assets` o `public`. Prefiere `src/assets` cuando la imagen se importe desde un componente Vue.
3. Importa la imagen local en `<script setup lang="ts">` si esta en `src/assets`. Si esta en `public`, usa una ruta absoluta desde `/` y no la importes.
4. Sustituye el placeholder por la referencia de la imagen en cada objeto `perfil`, o crea una propiedad reactiva compartida solo si todos los perfiles deben usar la misma imagen.
5. Renderiza el avatar antes del nombre de usuario con `:src="pub.perfil"` y un `:alt` descriptivo, evitando depender de una URL externa.
6. Aplica una clase especifica para el avatar. Mantiene dimensiones estables, `object-fit: cover`, forma circular y un tamaño adecuado para escritorio y movil sin afectar la imagen principal de la publicacion.
7. Revisa que no queden etiquetas HTML incompletas, imports sin uso ni referencias a archivos inexistentes en el componente modificado.
8. Ejecuta `npm run type-check` y, si el cambio afecta el build, `npm run build`.

## Criterios de finalizacion

- La imagen se carga desde el asset esperado y aparece junto al usuario correcto.
- El avatar tiene `alt` util y conserva una dimension estable en responsive.
- No quedan placeholders innecesarios ni URLs externas para el perfil.
- El type-check de Vue termina sin errores relacionados con el cambio.

## Decisiones

- Si cada publicacion pertenece a un usuario distinto, guarda `perfil` dentro de cada objeto.
- Si todas las publicaciones pertenecen al mismo perfil, usa una referencia compartida para evitar duplicacion.
- Si una imagen no existe, no inventes la ruta: solicita el archivo o usa temporalmente un placeholder explicito hasta recibirlo.
