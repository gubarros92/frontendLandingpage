<template>
    <section class="carrossel-premios">
      <h2>Prêmios</h2>
      <div class="carousel">
        <div v-for="prize in prizes" :key="prize.name" class="prize">
          <img :src="prize.image" alt="Prêmio">
          <p>{{ prize.name }}</p>
        </div>
      </div>
    </section>
  </template>
  <script>
  export default {
    name: 'CarrosselPremios',
    data() {
      return {
        prizes: [
          { name: 'Carro 0Km', image: 'https://via.placeholder.com/200x150?text=Carro+0Km' },
          { name: 'Moto', image: 'https://via.placeholder.com/200x150?text=Moto' },
          { name: 'Viagem', image: 'https://via.placeholder.com/200x150?text=Viagem' }
        ]
      }
    }
  }
  </script>
  
  <style scoped>
  .carousel {
    display: flex;
    overflow-x: scroll;
  }
  .prize {
    width: 200px;
    text-align: center;
    margin-right: 20px;
  }
  </style>
  