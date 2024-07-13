<template>
    <header>
      <h1>Truckme</h1>
      <nav>
        <ul>
          <li><a href="#">Início</a></li>
          <li><a href="#">Sobre</a></li>
          <li><a href="#">Serviços</a></li>
          <li><a href="#">Contato</a></li>
        </ul>
      </nav>
    </header>
  </template>
  
  <script>
  export default {
    name: 'HeaderComponent'
  }
  </script>
  
  <style scoped>
  header {
    background: #333;
    color: white;
    padding: 10px;
  }
  nav ul {
    list-style: none;
    padding: 0;
  }
  nav ul li {
    display: inline;
    margin-right: 20px;
  }
  nav ul li a {
    color: white;
    text-decoration: none;
  }
  </style>
