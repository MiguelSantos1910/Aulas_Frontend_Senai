<template>
  <footer>
    <p>© 2025 Agência de Viagens. Todos os direitos reservados.</p>
    <div class="social-media">
      <a href="#" aria-label="Facebook"><i class="fab fa-facebook-f"></i></a>
      <a href="#" aria-label="Twitter"><i class="fab fa-twitter"></i></a>
      <a href="#" aria-label="Instagram"><i class="fab fa-instagram"></i></a>
    </div>
  </footer>
</template>

<script>
export default {
  name: 'Footer'
}
</script>

<style scoped>
footer {
  text-align: center;
  padding: 20px;
  background-color: #f8f9fa;
  color: #6c757d;
  font-size: 14px;
}
p {
  margin: 0;
}
.social-media {
  margin-top: 10px;
}
.social-media a {
  margin: 0 10px;
  color: #6c757d;
  text-decoration: none;
}
.social-media a:hover {
  color: #007bff;
}
.social-media i {
  font-size: 20px;
}
</style>
