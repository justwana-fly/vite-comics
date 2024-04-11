<template>

    <div class="jumbotron">
            <!-- Sezione Jumbotron con immagine di sfondo -->
            <div class="jumbotron-image"></div>
        </div>
    
      <div class="main">
        <!-- Contenuto principale -->
        <div class="row container justify-content-center">
          <!-- Iterazione attraverso gli elementi dell'array comics -->
          <div v-for="(comic, index) in comics" :key="index" class="col-lg-2 col-md-3 col-sm-4 col-6">
            <!-- Card per ogni fumetto -->
            <div class="card">
              <!-- Immagine del fumetto con effetto hover -->
              <div class="image-container">
                <img :src="comic.thumb" class="card-img-top" alt="Thumbnail">
                <!-- Dettagli del fumetto -->
                <div class="card-body">
                  <h5 class="card-title">{{ comic.series }}</h5>
                  <!-- Prezzo che appare in hover -->
                  <p class="card-text hover-price">{{ comic.price }}</p>           
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </template>
    
    <script>
    // Importazione dell'array comics dal file ComicsArray.js
    import { comics } from '@/assets/ComicsArray.js';
    
    export default {
      name: 'MainComponent', // Nome del componente
      data() {
        return {
          comics: comics // Array di fumetti
        };
      }
    };
    </script>
    
    <style>
    /* Stili personalizzati per il tuo componente MainComponent.vue */
    </style>
    
    <style lang="scss" scoped>
    /* Stili SCSS per il tuo componente */
    * {
      padding: 0;
      margin: 0;
      box-sizing: border-box;
    }
    .jumbotron {
      position: relative;
      height: 300px; /* Altezza della sezione jumbotron */
      background-color: #333; /* Colore di sfondo */
    }
    
    .jumbotron-image {
      position: absolute;
      top: 50%; /* Posizionamento verticale al centro */
      left: 0;
      right: 0;
      width: 100%;
      height: 100%; /* Altezza dell'immagine di sfondo */
      background-image: url('/images/jumbotron.jpg'); /* Immagine di sfondo */
      background-size: cover; /* Ridimensiona l'immagine per coprire l'intera area */
      transform: translateY(-50%); /* Spostamento verticale per centrare l'immagine */
    }
    
    .container {
      margin: 0 auto; /* Centra il contenuto nel container */
    }
    
    img {
      width: 110px;
      height: 110px;
      object-fit: cover;
    }
    
    .main {
      background-color: #1C1C1C;
      padding: 30px;
    }
    
    .image-container {
      position: relative; 
    }
    h5 {
        font-size: 9px;
        color: white;
        background-color: #1C1C1C;
        
    }
    
    .hover-price {
      display: none; 
    }
    
    .image-container:hover .hover-price {
      display: block; 
      background-color: #1C1C1C;
      color: white;
    }
    
    .card {
      border: none;
      width: 110px;
      margin-bottom: 20px;
    }
    
    .col-2 {
      padding: 10px;
    }
    </style>
    