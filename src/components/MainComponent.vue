<template>
    <div>
      <div class="row">
        <div v-for="(comic, index) in comics" :key="index" class="col-md-4 mb-4">
          <div class="card">
            <img :src="comic.thumb" class="card-img-top" alt="Thumbnail">
            <div class="card-body">
              <h5 class="card-title">{{ comic.series }}</h5>
              <p class="card-text">{{ comic.price }}</p>
              <p class="card-text">{{ comic.type }}</p>
            </div>
          </div>
        </div>
      </div>
    </div>
  </template>
  
  <script>
  // Importa l'array comics dal file ComicsArray.js
  import { comics } from '@/assets/ComicsArray.js';
  
  export default {
    name: 'MainComponent', // Nome del componente
    data() {
      return {
        comics: comics
      };
    }
  };
  </script>
  
  <style>
  /* Stili personalizzati per il tuo componente MainComponent.vue */
  </style>
  

<style lang="scss" scoped>
* {
    padding: 0;
    margin: 0;
    box-sizing: border-box;
}
.container {
    margin: 0 auto;
}

main {
    background-color: #1C1C1C;
}

</style>