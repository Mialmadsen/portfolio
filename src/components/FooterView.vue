<template> 

    <footer class="bg-very-grey text-very-dark !mt-40">
        <div class="grid grid-cols-12 gap-4 h-30">
    
    <!-- Left Section -->
    <div class="col-span-1 col-start-2 font-family1 text-very-dark flex flex-col justify-start !pt-4">
        <RouterLink to="/">FORSIDE</RouterLink>
        <RouterLink to="/about">OM MIG</RouterLink>
        <RouterLink to="/portfolio">PORTFOLIO</RouterLink>
    </div>

    <!-- Center Social Icons -->
    <div class="col-start-11 flex items-center justify-end">
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

<script setup>

</script>

<style lang="scss" scoped>

</style>