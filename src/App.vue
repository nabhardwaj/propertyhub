<script setup>
import { RouterLink, RouterView } from 'vue-router'
import HelloWorld from './components/HelloWorld.vue'
import SiteLogo from './assets/logo.svg'
</script>

<template>
  <header>
    <div class="wrapper">
      <img :src="SiteLogo" class="logo" name="logo" alt="logo" width="40" />

      <nav>
        <RouterLink to="/">Home</RouterLink>
        <RouterLink to="/about">About</RouterLink>
        <RouterLink to="/publish-property">Post Property</RouterLink>
      </nav>
    </div>
  </header>

  <RouterView />
  <footer>

  </footer>
</template>

<style scoped>
header {
  line-height: 1.5;
  max-height: 100vh;
  padding: 1rem;
}

header .wrapper {
    display: flex;
    flex-direction: row;
    flex-wrap: wrap;
    align-items: center;
    flex: 1 1 auto;
    justify-content: space-between;
  }
.logo {
  display: block;
  margin-right: 2rem;
}

nav {
  font-size: 12px;
  text-align: center;
  display: flex;
}

nav a.router-link-exact-active {
  color: var(--color-text);
}

nav a.router-link-exact-active:hover {
  background-color: transparent;
}

nav a {
  display: inline-block;
  padding: 0 1rem;
  border-left: 1px solid var(--color-border);
}

nav a:first-of-type {
  border: 0;
}
footer{
  background:rgba(230,255,203,1);
  padding: 1rem;
}
@media (min-width: 1024px) {
  header {
    display: flex;
    place-items: center;
   
  }

  .logo {
    margin: 0 2rem 0 0;
  }

  header .wrapper {
    display: flex;
    flex-direction: row;
    flex-wrap: wrap;
    align-items: center;
    flex: 1 1 auto;
    justify-content: space-between;
  }

  nav {
    text-align: left;
    font-size: 1rem;
  }
}
</style>
