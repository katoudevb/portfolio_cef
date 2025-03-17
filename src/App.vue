<template>
  <div id="app">
    <Header />

    <RouterView />

    <Footer />
  </div>

  <RouterLink />
</template>

<script setup>
import { RouterLink, RouterView } from 'vue-router'
import Header from './components/Header.vue';
import Footer from './components/Footer.vue';
</script>
