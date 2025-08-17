<template>
  <div>
    <header>
      <h1>Agência de Viagem</h1>
      <div class="user-info">
        <p v-if="auth.isAuthenticated">Bem-vindo, {{ auth.getUser.name }}</p>
        <button v-if="!auth.isAuthenticated" @click="logInUser">Login</button>
        <button v-if="auth.isAuthenticated" @click="logout">Logout</button>
      </div>
      <div class="search-bar">
        <input type="text" placeholder="Pesquisar..." />
        <button>Pesquisar</button>
      </div>
      <div class="language-selector">
        <select>
          <option value="pt">Português</option>
          <option value="en">English</option>
          <option value="es">Español</option>
        </select>
        <div>
          <router-link to="/">Início</router-link>
          <router-link to="/sobre">Sobre</router-link>
          <router-link to="/services">Destinos</router-link>
          <router-link to="/login">Login</router-link>
        </div>
      </div>
    </header>
    <main>
      <router-view />
    </main>
  </div>
</template>

<script>
import { useAuthStore } from './stores/login.js'
export default {
  setup() {
    const auth = useAuthStore() 

    const logInUser = () => {

      auth.login({ name: 'Miguel' }, 'token123')
    }

    const logout = () => {
      auth.logout()
    }

    return { auth, logInUser, logout }
  }
}
</script>

<style scoped>
header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 20px;
  background-color: #007bff;
  color: white;
}
.user-info {
  display: flex;
  align-items: center;
}
.user-info button {
  margin-left: 10px;
}
.search-bar {
  display: flex;  
  align-items: center;
}
.search-bar input {
  padding: 5px;
  border: none;
  border-radius: 5px;
}
.search-bar button {
  padding: 5px 10px;
  background-color: #0056b3;
  color: white;
  border: none;
  border-radius: 5px;
  margin-left: 5px;
}
.language-selector {
  display: flex;
  align-items: center;
}
.language-selector select {
  margin-right: 10px;
  padding: 5px;
  border-radius: 5px;
}
.language-selector a {
  color: white;
  text-decoration: none;
  margin-left: 10px;
} 
.language-selector a:hover {
  text-decoration: underline;
}
main {
  padding: 20px;
}
</style>
