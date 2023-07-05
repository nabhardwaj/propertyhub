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
        <RouterLink to="/publish-property" class="postPrptyBtn"><span>Post Property</span></RouterLink>
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
  padding: .5rem 1rem;
  border-left: 1px solid var(--color-border);
}

nav a:first-of-type {
  border: 0;
}
nav a.postPrptyBtn{
  margin-right: 1rem;
  position: relative;
  overflow: hidden;
}
nav a.postPrptyBtn span{
  position: relative;
}
nav a.postPrptyBtn:before{
  content: '';
  position: absolute;
    top: 50%;
    left: 50%;
    right: 50%;
    bottom: 50%;
    border-radius: 8%;
    -moz-animation: rippleEffect 2s infinite;
    -webkit-animation: rippleEffect 2s infinite;
    background: var(--color-primary);
}
@-moz-keyframes rippleEffect {
  0% {top: 50%;left: 50%;right: 50%;bottom: 50%; opacity: 0.0;}
    50% {opacity: .8;}
    100% {top: -50%;left: -50%;right: -50%;bottom: -50%; opacity: 0.0;}
}

@-webkit-keyframes rippleEffect {
  /* 0% {-webkit-transform: scale(0.1, 0.1); opacity: 0.0;}
    50% {opacity: 1.0;}
    100% {-webkit-transform: scale(1.2, 1.2); opacity: 0.0;} */
    /* 0% {width:.5%; opacity: 0.0;}
    50% {opacity: .8;}
    100% {width: 100%; opacity: 0.0;} */
    0% {top: 50%;left: 50%;right: 50%;bottom: 50%; opacity: 0.0;}
    50% {opacity: .8;}
    100% {top: -50%;left: -50%;right: -50%;bottom: -50%; opacity: 0.0;}
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
