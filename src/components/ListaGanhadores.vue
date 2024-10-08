<template>
    <section class="lista-ganhadores">
      <h2>Lista de Ganhadores</h2>
      <div v-for="ganhador in ganhadores" :key="ganhador._id" class="ganhador">
        <h3 @click="toggle(ganhador._id)">{{ ganhador.name }}</h3>
        <p v-if="activeGanhador === ganhador._id">Prêmio: {{ ganhador.prize }} | Data: {{ ganhador.date }}</p>
      </div>
    </section>
  </template>
  
  <script>
  export default {
    name: 'ListaGanhadores',
    data() {
      return {
        ganhadores: [],
        activeGanhador: null
      }
    },
    methods: {
      fetchGanhadores() {
        fetch('https://sua-api-url/ganhadores') // Substitua pela URL da sua API
          .then(response => response.json())
          .then(data => {
            this.ganhadores = data;
          });
      },
      toggle(id) {
        this.activeGanhador = this.activeGanhador === id ? null : id;
      }
    },
    mounted() {
      this.fetchGanhadores();
    }
  }
  </script>
  
  <style scoped>
  h3 {
    cursor: pointer;
  }
  </style>
  