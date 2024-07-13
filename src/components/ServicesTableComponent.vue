<template>
    <section class="services-section">
      <h2>Nossos Serviços</h2>
      <div class="table-container">
        <table>
          <tr>
            <th>Serviço</th>
            <th>Descrição</th>
            <th>Preço por Km</th>
          </tr>
          <tr>
            <td>Carga geral</td>
            <td>Transferência de mercadorias não perigosas</td>
            <td>R$50,00</td>
          </tr>
          <tr>
            <td>Carga perigosa</td>
            <td>Transporte de mercadorias classificadas como perigosa</td>
            <td>R$100,00</td>
          </tr>
        </table>
      </div>
    </section>
  </template>
  
  <script>
  export default {
    name: 'ServicesTableComponent'
  }
  </script>
  
  <style scoped>
  .services-section {
    display: flex;
    flex-direction: column;
    align-items: center;
  }
  
  .table-container {
    width: 80%; /* Ajuste a largura conforme necessário */
    margin: 0 auto;
  }
  
  table {
    width: 50%;
    border-collapse: collapse;
  }
  
  th, td {
    border: 1px solid #ddd;
    padding: 8px;
    text-align: left; /* Ajuste o alinhamento conforme necessário */
  }
  
  th {
    background-color: #f2f2f2;
  }

  h2 {
    margin-right: 80%;

  }
  </style>
