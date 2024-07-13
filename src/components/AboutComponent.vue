<template>
    <section class="about-us">
      <div class="about-content">
        <div class="text-column">
          <h2>Sobre Nós</h2>
          <p v-if="!isExpanded">
            Na TruckMe, somos uma transportadora inovadora que combina tecnologia e eficiência para transformar o setor de logística. Com um aplicativo móvel desenvolvido para facilitar a conexão entre transportadores e indústrias, nosso objetivo é simplificar o processo de fechamento de fretes, tornando-o mais ágil e menos burocratizado.
            <span v-if="!isExpanded">...</span>
          </p>
          <p v-if="isExpanded">
            Na TruckMe, somos uma transportadora inovadora que combina tecnologia e eficiência para transformar o setor de logística. Com um aplicativo móvel desenvolvido para facilitar a conexão entre transportadores e indústrias, nosso objetivo é simplificar o processo de fechamento de fretes, tornando-o mais ágil e menos burocratizado.
            <br /><br />
            Acreditamos que a tecnologia pode revolucionar a maneira como as empresas se conectam e fazem negócios. Por isso, oferecemos uma plataforma intuitiva que permite que nossos clientes encontrem as melhores soluções de transporte de forma rápida e prática.
            <br /><br />
            Na TruckMe, nossa missão é proporcionar uma experiência fluida e eficiente, ajudando as indústrias a otimizar sua logística e os transportadores a maximizar suas oportunidades de trabalho. Estamos comprometidos em criar um futuro mais sustentável e conectado para o transporte de cargas.
          </p>
          <button @click="toggleExpand">{{ isExpanded ? 'Leia menos' : 'Leia mais' }}</button>
        </div>
        <div class="image-column">
          <img src="../assets/image-column1.png" alt="Sobre Nós" />
        </div>
      </div>
    </section>
  </template>
  
  <script>
  export default {
    name: 'AboutUsComponent',
    data() {
      return {
        isExpanded: false,
      };
    },
    methods: {
      toggleExpand() {
        this.isExpanded = !this.isExpanded;
      },
    },
  };
  </script>
  
  <style scoped>
  .about-us {
    display: flex;
    align-items: flex-start; 
    margin: 20px;
  }
  
  .about-content {
    display: flex;
    width: 100%;
  }
  
  .text-column {
    flex: 1;
    padding: 20px;
    text-align: justify;
  }
  
  .image-column {
    flex: 1;
    display: flex;
    justify-content: center;
    align-items: center;
  }
  
  .image-column img {
    max-width: 100%;
    height: auto;
  }
  
  button {
    margin-top: 15px;
    padding: 10px 15px;
    background-color: #4CAF50; /* Cor do botão */
    color: white;
    border: none;
    cursor: pointer;
  }
  
  button:hover {
    background-color: #45a049; /* Cor do botão ao passar o mouse */
  }
  </style>
  