<script setup>
import { RouterLink, RouterView } from 'vue-router'
import FooterView from '@/components/FooterView.vue'
import NavBar from '@/components/NavBar.vue'
</script>

<template>
  <header>
    <div class="wrapper w-full ">
      <NavBar />
    </div>
  </header>

  <RouterView />  

  <FooterView />

  
</template>

<style>



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
    place-items: flex-start;
    flex-wrap: wrap;
  }

  nav {
    margin-left: 2rem;
    margin-right: 2rem;
    font-size: 1rem;
    padding: 1rem 0;
    
  }
}
</style>
