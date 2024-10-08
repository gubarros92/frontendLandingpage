<template>
    <header class="hero-section">
      <nav>
        <h1>Nome do Evento</h1>
        <button @click="cadastrar">Cadastrar-se</button>
      </nav>
      <div class="banner">
        <h2>Participe e concorra a prêmios incríveis!</h2>
      </div>
    </header>
  </template>
  
  <script>
  export default {
    name: 'HeroSection',
    methods: {
      cadastrar() {
        alert('Botão de Cadastrar não funcional.');
      }
    }
  }
  </script>
  
  <style scoped>
  .hero-section {
    text-align: center;
    padding: 20px;
  }
  .banner {
    background-color: #f5f5f5;
    padding: 50px;
  }
  </style>
  