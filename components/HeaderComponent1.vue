<!-- HeaderComponent.vue -->
<template>
  <header class="header">
    <div class="logo">Ecommerce Store</div>
    <nav class="nav">
      <router-link to="/">Home</router-link>
      <router-link to="/about">About</router-link>
      <router-link to="/contact">Contact</router-link>
    </nav>
  </header>
</template>

<style scoped>
.header {
  background-color: #007BFF;
  color: white;
  padding: 10px;
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.logo {
  font-size: 24px;
  font-weight: bold;
}

.nav {
  display: flex;
}

.nav a {
  color: white;
  text-decoration: none;
  margin-left: 15px;
}

.nav a:hover {
  text-decoration: underline;
}
</style>
