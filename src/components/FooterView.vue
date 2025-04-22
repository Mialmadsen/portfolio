<script setup>

</script>

<template> 

    <footer class="bg-very-grey text-very-dark ">
        <div class="grid grid-cols-12 gap-4 h-30">
    
    <!-- Left Section -->
    <div class="col-span-1 col-start-2 font-family1 text-very-dark flex flex-col justify-start !pt-6">
        <RouterLink to="/">FORSIDE</RouterLink>
        <RouterLink to="/portfolio">PORTFOLIO</RouterLink>
        <RouterLink to="/about">OM MIG</RouterLink>
        
    </div>

    <!-- Center Social Icons -->
    <div class="icons col-start-11 flex items-center justify-end">
        <a href="https://www.instagram.com/mia_lybaek_madsen/profilecard/">
            <img alt="instagram logo" class="instagram" src="@/assets/instagram.svg" width="29" height="29" />
        </a>  
        <a href="https://www.linkedin.com/in/mialybaekmadsen/">
            <img alt="linkedin logo" class="linkedin" src="@/assets/linkedin.svg" width="31" height="31" />
        </a>
        <a href="https://www.facebook.com/mia.madsen.3194?locale=da_DK">
            <img alt="facebook logo" class="facebook" src="@/assets/facebook.svg" width="30" height="30" />
        </a>
    </div>

        </div>
    </footer>

</template>


<style>

footer {
    margin-top: 10rem;
}

.icons {
    gap: 0.5rem;
}



footer a:hover {
color: var(--color-very-light-grey);
}

@media (max-width: 768px) {

footer {
    padding: 1rem;
    margin-top: 3rem;
  }

  footer .grid {
    display: flex;                 
    flex-direction: column;       
    align-items: center;          
    gap: 2rem;
    text-align: center;
  }

  footer .col-span-1 {
    display: flex;               
    flex-direction: column;
    align-items: center;          
    gap: 0.5rem;
  }

  footer .col-start-11 {
    display: none;              
  }

  footer a {
    font-size: 0.7rem;
  }
}


</style>