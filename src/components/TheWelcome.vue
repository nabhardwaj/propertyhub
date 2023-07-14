<script setup>
import WelcomeItem from './WelcomeItem.vue'
import HomeSearchBox from './HomeSearchBox.vue'
</script>

<template>
  <WelcomeItem>
    <template #icon></template>
    <template #heading>Ashwagan</template>

    Ashla’s
    <a href="" target="_blank" rel="noopener">publish property</a>
    provides you with all functionality you need to get started.
  </WelcomeItem>
  <HomeSearchBox>
    <template #heading></template>
  </HomeSearchBox>
  
</template>
