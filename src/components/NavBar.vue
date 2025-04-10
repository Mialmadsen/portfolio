<template>
    <nav class="grid grid-cols-12 gap-4">
      

      <div class="col-span-3">
        <RouterLink class="" to="/">FORSIDE</RouterLink>
        <RouterLink class="" to="/about">OM MIG</RouterLink>
        <RouterLink class="" to="/portfolio">PORTFOLIO</RouterLink>
      </div>


        <div class="logo_wrapper col-span-6 flex justify-self-center">
          <img alt="Personal logo" class="logo col-span-2" src="@/assets/Logo 2.svg" width="50" height="50" />
        </div>
        <div class="socials_wrapper col-span-3 flex justify-self-end">
            <img alt="instagram logo" class="instagram" src="@/assets/instagram.svg" width="30" height="30" href="https://www.instagram.com/mia_lybaek_madsen/" />
            <img alt="linkedin logo" class="linkedin" src="@/assets/linkedin.svg" width="26" height="26" />
            <img alt="facebook logo" class="facebook" src="@/assets/facebook.svg" width="30" height="30" />
        </div>
    </nav>
</template>

<script setup>
import { RouterLink, RouterView } from 'vue-router'
</script>

<style scoped>

header {
  line-height: 1.5;
  max-height: 100vh;
  width: 100%;
  display: flex;
}

nav {
  width: 100%;
  font-size: 12px;
  font-family: impact, sans-serif;
  color: #1C1713;
  
}

.wrapper {
  
}

.logo {
  display: flex;
  justify-self: center;

}


nav a.router-link-exact-active {
  color: var(--color-text);
}

nav a.router-link-exact-active:hover {
  background-color: transparent;
}

nav a {
  display: inline-block;
  padding-left: 1rem;
 
}

nav a:first-of-type {
  border: 0;
}

.socials_wrapper {
    display: flex;
}

.socials_wrapper img {
    margin: 0.2rem;
}
</style>