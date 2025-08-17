<template>
  <header>
    <h1>Agência de Viagem</h1>
    <nav>
      <ul>
        <li><router-link to="/">Início</router-link></li>
        <li><router-link to="/sobre">Sobre</router-link></li>
        <li><router-link to="/services">Destinos</router-link></li>
        <li><router-link to="/login">Login</router-link></li>
      </ul>
    </nav>
    <div v-if="auth.isAuthenticated">
      Bem-vindo, {{ auth.getUser.name }}!
      <button @click="logout">Logout</button>
    </div>
  </header>
</template>

<script>
import { useAuthStore } from '../stores/login.js'  

export default {
  name: 'Header',
  setup() {
    const auth = useAuthStore()  

    const logout = () => {
      auth.logout()
    }

    return { auth, logout }
  }
}
</script>

<style scoped>
header {
  background-color: #f8f9fa;
  padding: 10px;
  text-align: center;
}
nav ul {
  list-style-type: none;
  padding: 0;
}
nav ul li {
  display: inline;
  margin: 0 15px;
}
nav ul li a {
  text-decoration: none;
  color: #007bff;
}
nav ul li a:hover {
  text-decoration: underline;
}
h1 {
  margin: 0;
  font-size: 24px;
  color: #343a40;
}
</style>
