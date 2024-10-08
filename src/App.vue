<template>
    <div id="app">
      <HeroSection />
      <ComoParticipar />
      <CarrosselPremios />
      <Faq />
      <ListaGanhadores />
      <Footer />
    </div>
  </template>
  
  <script>
  import HeroSection from './components/HeroSection.vue';
  import ComoParticipar from './components/ComoParticipar.vue';
  import CarrosselPremios from './components/CarrosselPremios.vue';
  import Faq from './components/Faq.vue';
  import ListaGanhadores from './components/ListaGanhadores.vue';
  import Footer from './components/Footer.vue';
  
  export default {
    name: 'App',
    components: {
      HeroSection,
      ComoParticipar,
      CarrosselPremios,
      Faq,
      ListaGanhadores,
      Footer
    }
  }
  </script>
  
  <style>
  #app {
    font-family: Avenir, Helvetica, Arial, sans-serif;
    text-align: center;
    color: #2c3e50;
    margin-top: 60px;
  }
  </style>
  