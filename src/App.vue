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
