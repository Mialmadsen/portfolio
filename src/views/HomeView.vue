<script setup>

</script>

<template>
  <main>
    <!-- Hero Section -->
    <div class="relative w-full h-180 overflow-hidden">
      <!-- Hero Image -->
      <img src="../assets/hero.png" alt="Home Hero Image" class="absolute top-0 left-0 w-full h-180 object-cover" />
      <!-- Centered Text -->
      <div class="absolute inset-0 flex flex-col items-center justify-center text-center">
        <h1 class="font-family1 text-very-dark text-5xl !mb-4">
          MIA LYBÆK MADSEN
        </h1>
        <h2 class="font-family1 text-very-dark text-2xl">
          MULTIMEDIEDESIGNER & CONTENT CREATOR & WEBDEVELOPER
        </h2>
      </div>
    </div>

    <!-- Webudvikling section -->
      <div class="webudviking-section grid grid-cols-12 gap-4 !mt-40">
        <!-- Image spans 6 columns -->
        <div class="col-span-7 mx-auto overflow-hidden h-125">
          <img src="../assets/Plastic website.png" alt="webudvikling Image" class="w-full object-cover" />
        </div>
        <!-- Text spans 5 columns -->
        <div class="col-span-4 !ml-20">
          <h3 class="font-family1 text-very-dark text-4xl !mb-4">
            Webudvikling
          </h3>
          <p class="font-family3 text-very-dark text-lg">
            Jeg er en passioneret webudvikler med erfaring i at skabe brugervenlige og æstetisk tiltalende hjemmesider. Jeg elsker at kombinere kreativitet med teknisk kunnen for at levere skræddersyede løsninger, der opfylder kundernes behov.
          </p>
        </div>
      </div>

    <!-- Content Creation section -->
      <div class="content-creation-section grid grid-cols-12 gap-4 !mt-40">
        <!-- Text spans 5 columns -->
        <div class="col-span-4 col-start-2 !mr-20">
          <h3 class="font-family1 text-very-dark text-4xl !mb-4">
            Content Creation
          </h3>
          <p class="font-family3 text-very-dark text-lg">
            Jeg er en kreativ indholdsskaber med en passion for at fortælle historier gennem visuelle medier. Jeg skaber engagerende indhold, der fanger opmærksomheden og formidler budskaber effektivt. Uanset om det er billeder, videoer eller grafik, stræber jeg efter at skabe indhold, der inspirerer og engagerer.
          </p>
        </div>
        <!-- Image spans 6 columns -->
        <div class="col-span-7 mx-auto overflow-hidden h-125">
          <img src="../assets/coffeeposter.png" alt="webudvikling Image" class="w-full object-contain" />
        </div>
      </div>

    <!-- Kontakt mig section -->
      <div class="kontakt-mig-section flex flex-col items-center justify-center !mt-40">
        <h3 class="font-family1 text-very-dark text-4xl !mb-4">
          Kontakt Mig
        </h3>
        <p class="font-family2 text-very-dark text-lg !pb-4">
          Er du interesseret i at samarbejde eller har du spørgsmål? Tøv ikke med at kontakte mig!
        </p>
        <p class="font-family3 text-very-dark text-lg">
          Email: mia.l.madsen@live.dk
        </p>
        <p class="font-family3 text-very-dark text-lg">
          Telefon: 26166752
        </p>
        <div class="socials_wrapper col-span-3 flex justify-self-center !pt-4 gap-4">
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
  
  
  </main>
</template>

<style scoped>
  .socials_wrapper img:hover {
    cursor: pointer;
  }
</style>
