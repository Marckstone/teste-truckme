<template>
    <section class="banner-container">
      <img src="../assets/banner.png" alt="Banner" class="banner-image" />
      <div class="banner-text">
        Bem-vindo à TruckMe
      </div>
    </section>
  </template>
  
  <script>
  export default {
    name: 'BannerComponent'
  }
  </script>
  
  <style>
  .banner-container {
    position: relative;
    width: 100%;
    overflow: hidden;
    margin: 0;
    padding: 0;
  }
  
  .banner-image {
    width: 100%;
    height: auto; /* Ajusta a altura automaticamente */
    display: block;
  }
  
  .banner-text {
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    color: white; /* Cor do texto */
    font-size: 3rem; /* Aumentar o tamanho da fonte */
    text-align: center; /* Centralizar o texto */
    text-shadow: 2px 2px 5px rgba(0, 0, 0, 0.7); /* Sombra do texto */
    transition: transform 0.3s ease; /* Transição suave */
  }
  
  /* Efeito de transição ao passar o mouse */
  .banner-container:hover .banner-text {
    transform: translate(-50%, -50%) scale(1.05); /* Aumenta o texto ao passar o mouse */
  }
  </style>
  