<script setup>
import Carousel from '../components/Carousel.vue'
</script>

<template>
  <main class="projects-page">
    <h1 class="pageTitle"> Projects </h1>
    <Carousel/>
  </main>
  
</template>

<style scoped>
  .pageTitle{
    color: azure;
    font: bold;
    text-align: center;
    padding-top: 48px;
  }

  .projects-page{
    flex-direction: row;
  }
</style>