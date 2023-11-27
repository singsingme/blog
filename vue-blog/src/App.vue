<script setup>
import { RouterLink, RouterView } from 'vue-router'
import HelloWorld from './components/HelloWorld.vue'
import Tiptap from './components/Tiptap.vue'

</script>

<template>
  <header>
    <nav>
      <RouterLink to="/">Home</RouterLink>
      <RouterLink to="/about">About</RouterLink>
      <RouterLink to="/WriteArticle">WriteArticle</RouterLink>
    </nav>
  </header>

  <RouterView />
</template>

<style scoped>

nav {
  width: 100%;
  background-color: rgb(102, 255, 0);
  color: white;
  margin-right: 20px;
}

</style>
