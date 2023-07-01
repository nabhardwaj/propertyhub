<script setup>
import { RouterLink, RouterView } from 'vue-router'
import HelloWorld from './components/HelloWorld.vue'
import SiteLogo from './assets/logo.svg'
import TheFooter from './components/TheFooter.vue'
</script>

<template>
  <header>
    <div class="wrapper">
      <img :src="SiteLogo" class="logo" name="logo" alt="logo" width="40" />

      <nav>
        <RouterLink to="/">Home</RouterLink>
        <RouterLink to="/about">About</RouterLink>
        <RouterLink to="/publish-property">Post Property</RouterLink>
        <a class="userProfileMenu">
          <img src="./assets/user.png" name="usericon" alt="user" width="20" height="20" />
          <!-- <nav class="userProfileMenuList">
            <a href="">Login</a>
            <a href="">Dashboard</a>
            <a href="">Property List</a>
          </nav> -->
        </a>
      </nav>
    </div>
  </header>

  <RouterView />
  <TheFooter />
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
  place-items: center;
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
.userProfileMenu{
  padding: 10px;
  background: var(--color-primary);
  border-radius: 50%;
  display: flex;
  place-items: center;
  position:relative;
  cursor: pointer;
}
.userProfileMenuList{
  position: absolute;
  right: 0px;
  top: 15px;
  width: 150px;
  height: 0px;
  padding: 5px;
  box-shadow: 1px 1px 10px var(--color-primary);
  -webkit-box-shadow: 1px 1px 10px var(--color-primary);
}
.userProfileMenu:hover > .userProfileMenuList , .userProfileMenu:active > .userProfileMenuList{
  display: block;
  height: auto;
  transition: height ease-in-out 1s;
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
