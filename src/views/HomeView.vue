<script setup>
import { onMounted, ref } from "vue";

const velkommenSection = ref(null);

onMounted(() => {
  const observer = new IntersectionObserver(
    (entries) => {
      entries.forEach((entry) => {
        if (entry.isIntersecting) {
          entry.target.classList.remove("opacity-0", "translate-x-20");
          entry.target.classList.add("opacity-100", "translate-x-0");
        }
      });
    },
    { threshold: 0.2 } // Aktiver når 20% af sektionen er synlig
  );

  if (velkommenSection.value) observer.observe(velkommenSection.value);
});
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

  <!-- Velkommen section -->
<div class="velkommen-section grid grid-cols-12 h-125 !mt-40 opacity-0 translate-x-20 transition-all duration-700" ref="velkommenSection">
  <div class="velkommen-container col-span-8 col-start-3 h-125 bg-very-light-grey flex items-center">
    <div class="velkommen-text-box">
      <h3 class="font-family1 text-very-dark text-4xl !ml-20 sm:ml-0 sm:text-2xl sm:align-left">
        Velkommen til!
      </h3>
      <p class="font-family3 text-very-dark text-lg !w-1/2 !ml-20 !mt-4 sm:w-full sm:ml-0 sm:text-left">
        Mit navn er Mia Lybæk Madsen - og dette er min portfolio-hjemmeside. 
        Her kan du læse om mig både proffesionelt og personligt, samt få et indblik i hvilke evner og kompetencer jeg har tillært mig indenfor verdenen som multimediedesigner. 
        Udforsk nogle af mine seneste projekter og kreationer, og lær mig bedre at kende som person. 
        Og tøv endelig ikke med at kontakte mig! 
        God fornøjelse!
      </p>
    </div>
    <img src="../assets/welcome img.png" alt="welcome Image" class="!w-1/3 justify-self-end !mb-1" />
  </div>
</div>


    <!-- Webudvikling section -->
      <div class="webudviking-section grid grid-cols-12 gap-4 !mt-50">
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
            Den ene del af multimediedesign-verdenen for mig handler om at ideudvikle, designe og kode nye hjemmesider, samt vedligeholde og skabe nyt indhold på allerede eksisterende hjemmesider. Her har jeg kendskab til Figma, HTML, CSS, JavaScript, Vuejs, Tailwind, Github, Wordpress og en smule php. Undervejs på min uddannelse, har vi udviklet flere projekter, hvor vi har skulle bruge og vise vores evner indenfor disse områder. Et par eksempler kan ses på min portfolioside. 
          </p>
        </div>
      </div>

    <!-- Content Creation section -->
      <div class="content-creation-section grid grid-cols-12 gap-4 !mt-50">
        <!-- Text spans 5 columns -->
        <div class="col-span-4 col-start-2 !mr-20">
          <h3 class="font-family1 text-very-dark text-4xl !mb-4">
            Content Creation
          </h3>
          <p class="font-family3 text-very-dark text-lg">
            Den anden del af multimediedesign-verdenen for mig handler om at skabe fangende, æstetisk og engagerende content som alt lige fra logoer, plakater og visitkort til produktbilleder, reklamevideoer, animationer og meget mere.
            Her har jeg kendskab til Adobe programmerne: Indesign, Illustrator, Photoshop, Premiere Pro og After Effects, samt andre værktøjer som Canva, Canva Pro og Figjam. Eksempler på dette kan også ses på min portfolioside.
          </p>
        </div>
        <!-- Image spans 6 columns -->
        <div class="col-span-7 mx-auto overflow-hidden h-125">
          <img src="../assets/coffeeposter.png" alt="webudvikling Image" class="w-full object-contain" />
        </div>
      </div>

    <!-- Kontakt mig section -->
    <div class="kontakt-mig-section grid grid-cols-12 !mt-50">
  <div class="col-span-8 col-start-3 h-125 bg-very-light-grey flex flex-col items-center justify-center text-center">
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
    <div class="socials_wrapper flex gap-4 !mt-4">
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
</div>
  
  
  </main>
</template>

<style>
  .socials_wrapper img:hover {
    cursor: pointer;
  }


  @media (max-width: 768px) {
   
    /* Hero Section */
    .relative {
      height: 30vh;
    }

    .relative img {
      height: 30vh;
      width: 100%;
      object-fit: cover;
    }
    .relative h1 {
      font-size: 2rem;
    }

    .relative h2 {
      font-size: 1rem;
    }


  /* Velkommen Section */
  .velkommen-section {
    height: auto; 
    padding: 1rem; 
    grid-template-columns: 1fr; 
    
  }

  .velkommen-section.grid {
    margin-top: 1rem;
  }

  .velkommen-container {
    align-items: center; 
    height: auto; 
    padding: 1rem; 
    box-sizing: border-box; 
    width: 100%; 
    margin-top: 0 !important; /* Fjern margin-top */
  }

  .velkommen-container img {
    display: none;
  }

  .velkommen-text-box {
    width: 100%; 
    padding: 1rem; 
    box-sizing: border-box; 
    margin: none; 
  }
  .velkommen-text-box h3 {
    font-size: 1rem; 
    margin: none; 
    padding-bottom: 1rem;
  }

  .velkommen-text-box p {
    font-size: 0.7rem; 
    margin: none; 
    width: 100%; 
  }







  
  











}


</style>
