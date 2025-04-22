<script setup>
import { ref } from 'vue'
import { RouterLink } from 'vue-router'

const isOpen = ref(false) // Reaktiv variabel til at styre, om mobilmenuen er åben eller lukket
</script>

<template>
  <nav class="w-full p-4 font-family1 text-very-dark">
    <!-- Desktop nav -->
    <div class="hidden md:grid grid-cols-12 gap-4 items-center">
      <!-- Links -->
      <div class="left col-span-3 flex space-x-4">
        <RouterLink to="/">FORSIDE</RouterLink>
        <RouterLink to="/portfolio">PORTFOLIO</RouterLink>
        <RouterLink to="/about">OM MIG</RouterLink>
      </div>

      <!-- Logo -->
      <div class="col-span-6 flex justify-center">
        <img alt="Personal logo" src="@/assets/Logo 2.svg" width="50" height="50" />
      </div>

      <!-- Socials -->
      <div class="col-span-3 flex justify-end gap-4 !pr-0">
        <a href="https://www.instagram.com/mia_lybaek_madsen/profilecard/">
          <img src="@/assets/instagram.svg" alt="Instagram" width="28" height="28" class="instalogo" />
        </a>
        <a href="https://www.linkedin.com/in/mialybaekmadsen/">
          <img src="@/assets/linkedin.svg" alt="LinkedIn" width="30" height="30" />
        </a>
        <a href="https://www.facebook.com/mia.madsen.3194?locale=da_DK">
          <img src="@/assets/facebook.svg" alt="Facebook" width="29" height="29" class="facebooklogo" />
        </a>
      </div>
    </div>

<!-- Mobil topbar -->
<div class="md:hidden flex justify-between items-center w-full">
  <!-- Logo -->
  <div class="!p-1">
    <img src="@/assets/Logo 2.svg" alt="Logo" width="30" height="30" />
  </div>

  <!-- Burger eller X ikon / knappen til at åbne menuen -->
  <button @click="isOpen = !isOpen" class="pr-2 focus:outline-none"> <!-- Når knappen klikkes, ændres `isOpen` mellem `true` og `false` -->
    <template v-if="isOpen"> <!-- Hvis `isOpen` er true, vises X-ikonet -->
      <!-- X ikon -->
      <svg class="w-6 h-6 text-very-dark" fill="none" stroke="currentColor" stroke-width="2"
           viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
        <path stroke-linecap="round" stroke-linejoin="round" d="M6 18L18 6M6 6l12 12"></path>
      </svg>
    </template>
    <template v-else> <!-- Hvis `isOpen` er false, vises burgerikonet -->
      <!-- Burger ikon -->
      <svg class="w-6 h-6 text-very-dark" fill="none" stroke="currentColor" stroke-width="2"
           viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
        <path stroke-linecap="round" stroke-linejoin="round"
              d="M4 6h16M4 12h16M4 18h16"></path>
      </svg>
    </template>
  </button>
</div>

    <!-- Mobil menu fade animation-->
    <transition name="mobile-fade-slide">
    <div v-if="isOpen" class="md:hidden mt-4 flex flex-col !space-y-2 text-center"> <!-- Mobilmenuen vises kun, hvis `isOpen` er true -->
      <!-- Link til forsiden. Når der klikkes, sættes `isOpen` til false for at lukke menuen -->
      <RouterLink to="/" @click="isOpen = false">FORSIDE</RouterLink>
      <!-- Link til portfolio. Lukker menuen, når der klikkes -->
      <RouterLink to="/portfolio" @click="isOpen = false">PORTFOLIO</RouterLink>
      <!-- Link til "Om mig". Lukker menuen, når der klikkes -->
      <RouterLink to="/about" @click="isOpen = false">OM MIG</RouterLink>
      <div class="flex justify-center !gap-1 !mt-3 !mb-6">
        <a href="https://www.instagram.com/mia_lybaek_madsen/profilecard/">
          <img src="@/assets/instagram.svg" alt="Instagram" width="20" height="20" class="instalogo" />
        </a>
        <a href="https://www.linkedin.com/in/mialybaekmadsen/">
          <img src="@/assets/linkedin.svg" alt="LinkedIn" width="22" height="22" />
        </a>
        <a href="https://www.facebook.com/mia.madsen.3194?locale=da_DK">
          <img src="@/assets/facebook.svg" alt="Facebook" width="21" height="21" class="facebooklogo-mobile" />
        </a>
      </div>
    </div>
  </transition>
  </nav>
</template>


<style>

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

.logo {
  display: flex;
  justify-self: center;

}

.instalogo {
  padding-top: 1px;
}

.facebooklogo {
  padding-top: 0.7px;
}

.facebooklogo-mobile {
  padding-top: 0.3px;
}




nav a.router-link-exact-active {
  color: var(--color-very-grey);
}

nav a.router-link-exact-active:hover {
  background-color: transparent;
}

nav a {
  display: inline-block;
}

.left a,
.menu a {
  padding-right: 2rem;
}


nav a:hover {
  color: var(--color-very-grey);
}

nav a:first-of-type {
  border: 0;
}

.socials_wrapper_nav {
  display: flex;
  justify-self: end;
  gap: 1rem;
}

.socials_wrapper_nav img:hover {
  cursor: pointer;
  
}

.socials_wrapper_nav a {
  padding-right: 0;
}

/* Media query for mobile devices */
.mobile-fade-slide-enter-active,
.mobile-fade-slide-leave-active {
  transition: all 0.3s ease;
}
.mobile-fade-slide-enter-from {
  opacity: 0;
  transform: translateY(-10px);
}
.mobile-fade-slide-enter-to {
  opacity: 1;
  transform: translateY(0);
}
.mobile-fade-slide-leave-from {
  opacity: 1;
  transform: translateY(0);
}
.mobile-fade-slide-leave-to {
  opacity: 0;
  transform: translateY(-10px);
}




</style>