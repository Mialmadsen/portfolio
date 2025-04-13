<script setup>

</script>

<template>
  <main>

    <!-- Hero Section -->
    <div class="relative w-full h-200 overflow-hidden">
      <!-- Hero Image -->
      <img src="../assets/hero3.jpg" alt="Home Hero Image" class="absolute top-0 left-0 w-full h-300 object-cover" />
      
      <!-- Centered Text -->
      <div class="absolute inset-0 flex flex-col items-center justify-center text-center">
        <h1 class="font-family1 text-butter-yellow text-5xl !mb-4">
          OM MIG
        </h1>
      </div>
    </div>

    <!-- cv & businesscard section -->
    <div class="cv-businesscard-section flex flex-row items-center justify-center !mt-20 !mb-20">
      <a 
        href="/assets/CV.pdf" 
        target="_blank" 
        rel="noopener noreferrer" 
        class="bg-very-grey text-butter-yellow font-family1 w-30 h-20 flex items-center justify-center !mr-10">
        CV
      </a>
      <a 
        href="/assets/.businesscard.pdf" 
        target="_blank" 
        rel="noopener noreferrer" 
        class="bg-very-grey text-butter-yellow font-family1 w-30 h-20 flex items-center justify-center !ml-10">
        Visitkort
      </a>
    </div>

    <!-- Video cv section -->
    <div class="video-cv-section flex justify-center items-center !mt-10">
      <iframe width="800" height="450" src="https://www.youtube.com/embed/lAhP_2eKS8I?si=xJEzl8vM0EBMGp7K" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
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