<template>
    <section class="faq">
      <h2>Perguntas Frequentes</h2>
      <div v-for="(faq, index) in faqs" :key="index" class="faq-item">
        <h3 @click="toggle(index)">{{ faq.question }}</h3>
        <p v-if="activeIndex === index">{{ faq.answer }}</p>
      </div>
    </section>
  </template>
  
  <script>
  export default {
    name: 'Faq',
    data() {
      return {
        activeIndex: null,
        faqs: [
          { question: 'Como funciona?', answer: 'Resposta sobre como funciona.' },
          { question: 'Qual o prazo?', answer: 'Resposta sobre prazo.' },
          { question: 'Como retirar o prêmio?', answer: 'Resposta sobre retirada de prêmio.' }
        ]
      }
    },
    methods: {
      toggle(index) {
        this.activeIndex = this.activeIndex === index ? null : index;
      }
    }
  }
  </script>
  
  <style scoped>
  .faq-item {
    cursor: pointer;
  }
  </style>
  