<template>
  <Header/>
    <section>
      <h2>Sobre Nós</h2>
      <p>Somos especialistas em viagens inesquecíveis.</p>
    </section>
  <Footer/>
</template>
<script>
  import Header from '../components/Header.vue';
  import Footer from '../components/Footer.vue';
  export default {
    name: 'Sobre',
    components: {
      Header,
      Footer
    }
  }
</script>
<style scoped>
  section {
    padding: 20px;
    background-color: #f9f9f9;
  }
  h2 {
    color: #333;  
    font-size: 24px;
  }
  p {
    color: #666;
    font-size: 16px;
  }
</style>