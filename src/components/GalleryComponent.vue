<template>
    <section>
      <h2>Galeria</h2>
      <div class="gallery-container">
        <button @click="prevImage" :disabled="currentIndex === 0">Anterior</button>
        <img :src="images[currentIndex]" class="gallery-image" />
        <button @click="nextImage" :disabled="currentIndex === images.length - 1">Próximo</button>
      </div>
      <div class="thumbnails">
        <img v-for="(image, index) in images" :key="index" :src="image" class="thumbnail" @click="setImage(index)" />
      </div>
    </section>
  </template>
  
  <script>
  export default {
    name: 'GalleryComponent',
    data() {
      return {
        currentIndex: 0,
        images: [
          require('../assets/image1.png'),
          require('../assets/image2.png'),
          require('../assets/image3.png'),
          require('../assets/image4.png'),
          require('../assets/image6.png'),
          require('../assets/image7.png'),
          require('../assets/image8.png')
        ]
      }
    },
    methods: {
      prevImage() {
        if (this.currentIndex > 0) {
          this.currentIndex--;
        }
      },
      nextImage() {
        if (this.currentIndex < this.images.length - 1) {
          this.currentIndex++;
        }
      },
      setImage(index) {
        this.currentIndex = index;
      }
    }
  }
  </script>
  
  <style scoped>
  .gallery-container {
    display: flex;
    align-items: center;
    justify-content: center;
    margin: 20px 0;
  }
  
  .gallery-image {
    max-width: 80%;
    height: auto;
    margin: 0 20px; /* Espaço entre os botões e a imagem */
  }
  
  button {
    padding: 10px 15px;
    background-color: #4CAF50;
    color: white;
    border: none;
    cursor: pointer;
    border-radius: 5px;
  }
  
  button:disabled {
    background-color: #ccc; /* Cor do botão desativado */
    cursor: not-allowed;
  }
  
  button:hover:not(:disabled) {
    background-color: #45a049;
  }
  
  .thumbnails {
    display: flex;
    justify-content: center;
    flex-wrap: wrap;
    margin-top: 20px;
  }
  
  .thumbnail {
    width: 100px;
    height: auto;
    margin: 5px;
    cursor: pointer;
    border: 2px solid transparent;
  }
  
  .thumbnail:hover {
    border-color: #4CAF50; /* Destaque ao passar o mouse */
  }
  </style>
  