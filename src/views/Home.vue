<template>
  <Header/>
    <section>
      <h2>Página Inicial</h2>
      <p>Bem-vindo à Agência de Viagem!</p>
      <div class="cards">
        <div class="card">
          <h3>Pacotes de Viagem</h3>
          <p>Descubra nossos pacotes de viagem exclusivos.</p>
        </div>
        <div class="card">
          <h3>Destinos Populares</h3>
          <p>Explore os destinos mais populares do mundo.</p>
        </div>
        <div class="card">
          <h3>Ofertas Especiais</h3>
          <p>Aproveite nossas ofertas especiais e promoções.</p>
        </div>
      </div>
      <h2>Descubra o Mundo</h2>
      <p>Viaje para lugares incríveis e crie memórias inesquecíveis.</p>
      <h2>Planeje Sua Viagem</h2>
      <p>Planeje sua próxima aventura com facilidade e conforto.</p>
      <h2>Explore Nossos Pacotes</h2>
      <p>Encontre o pacote de viagem ideal para você.</p>
      <h2>Viaje Conosco</h2>
      <p>Viaje com a gente e descubra o mundo de uma maneira única.</p>
      <div class="cards">
        <div class="card">
          <h3>Suporte ao Cliente</h3>
          <p>Estamos aqui para ajudar você a planejar sua viagem.</p>
        </div>
        <div class="card">
          <h3>Blog de Viagens</h3>
          <p>Leia nossos artigos e dicas de viagem.</p>
        </div>
        <div class="card">
          <h3>Contato</h3>
          <p>Entre em contato conosco para mais informações.</p>
        </div>
      </div>
      <h2>Junte-se a Nós</h2>
      <p>Inscreva-se para receber novidades e ofertas exclusivas.</p>
      <input type="email" placeholder="Seu email" />
      <button>Inscrever-se</button>
      <h2>Fale Conosco</h2>
      <p>Estamos sempre prontos para ouvir você.</p>
    </section>
  <Footer/>
</template>
<script>
  import Header from '../components/Header.vue';
  import Footer from '../components/Footer.vue';
  export default {
    name: 'Home',
    components: {
      Header,
      Footer
    }
  }
</script>
<style scoped>
  .cards {
    display: flex;
    justify-content: space-around;
    margin-top: 20px;
  }
  .card {
    background-color: #fff;
    border: 1px solid #ddd;
    border-radius: 8px;
    padding: 20px;
    width: 30%;
    box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
  }
  .card h3 {
    color: #333;
    font-size: 20px;
  }
  .card p {
    color: #666;
    font-size: 14px;
  }
  header, footer {
    background-color: #f8f8f8;
    padding: 10px 20px;
    text-align: center;
  }
  header h1, footer p {
    margin: 0;
    color: #333;
  }
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
  input[type="email"] {
    padding: 10px;
    width: 200px;
    margin-right: 10px;
    border: 1px solid #ddd;
    border-radius: 4px;
  }
  button {
    padding: 10px 20px;
    background-color: #007bff;
    color: white;
    border: none;
    border-radius: 4px;
    cursor: pointer;
  }
  button:hover {
    background-color: #0056b3;
  } 
</style>