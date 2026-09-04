<script setup lang="ts">
import Header from './components/Header.vue';
import ObjectoLiterals from './components/ObjectoLiterals.vue';

</script>

<template>
<Header></Header>

<main class="page-content">
  <section id="inicio">
    <div class="inicio">
      Hola
    </div>
  </section>
  <ObjectoLiterals></ObjectoLiterals>
  <h1>You did it!</h1>
  <p>
    Visit <a href="https://vuejs.org/" target="_blank" rel="noopener">vuejs.org</a> to read the
    documentation
  </p>
</main>
</template>

<style scoped>
.page-content {
  margin-left: 240px;
  padding: 24px;
}

.inicio {
  height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  font-size: 200px;
}
</style>
