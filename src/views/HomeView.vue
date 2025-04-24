<script setup>
import { onMounted, ref } from "vue"; 
// Hjælp fra Copilot og Chat GPT start
// Importerer `onMounted` og `ref` fra Vue. 
// `ref` bruges til at oprette en reaktiv reference, og `onMounted` bruges til at udføre kode, når komponenten er monteret.

const velkommenSection = ref(null); 
// Opretter en reaktiv reference `velkommenSection`, som initialiseres til `null`. 
// Denne reference vil blive bundet til HTML-elementet for "Velkommen-sektionen" via `ref="velkommenSection"`.

onMounted(() => { 
  // `onMounted` sikrer, at koden indeni kun køres, når komponenten bliver synlig når man scroller ned.

  const observer = new IntersectionObserver(
    (entries) => { 
      // Opretter en ny `IntersectionObserver`, som overvåger, om elementer kommer ind i eller forlader viewporten.
      entries.forEach((entry) => { 
        // Itererer gennem alle de observerede elementer (`entries`).
        if (entry.isIntersecting) { 
          // Tjekker, om elementet er synligt i viewporten (dvs. mindst 20% af det er synligt).
          entry.target.classList.remove("opacity-0", "translate-x-20"); 
          // Fjerner CSS-klasserne `opacity-0` og `translate-x-20`
          entry.target.classList.add("opacity-100", "translate-x-0"); 
          // Tilføjer CSS-klasserne `opacity-100` og `translate-x-0`, som gør elementet synligt og flytter det til sin oprindelige position.
        }
      });
    },
    { threshold: 0.2 } 
    // Konfigurerer observeren til at trigge, når mindst 20% af elementet er synligt i viewporten.
  );

  if (velkommenSection.value) observer.observe(velkommenSection.value); 
  // Starter observeren og overvåger det element, der er bundet til `velkommenSection`.
});
// Hjælp fra Copilot og Chat GPT
</script>

<template>
  <main class="overflow-hidden">
    <!-- Hero Section -->
    <div class="relative w-full h-200 overflow-hidden">
      <img src="../assets/hero.png" alt="Home Hero Image" class="absolute top-0 left-0 w-full h-200 object-cover" />
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
<div class="velkommen-section grid grid-cols-12 h-125 opacity-0 translate-x-20 transition-all duration-700" ref="velkommenSection"> <!-- Binder HTML-elementet til den reaktive reference velkommenSection, som er defineret i scriptet-->
  <div class="velkommen-container col-span-8 col-start-3 h-125 bg-very-light-grey flex items-center">
    <div class="velkommen-text-box">
      <h3 class="font-family1 text-very-dark text-4xl sm:text-4xl sm:align-left !pb-4">
        Velkommen til!
      </h3>
      <p class="font-family3 text-very-dark text-lg sm:w-full sm:ml-0 sm:text-left">
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
  <div class="webudviking-section grid grid-cols-12 gap-4">
    <div class="col-span-7 mx-auto overflow-hidden h-125">
      <img src="../assets/Plastic website.png" alt="webudvikling Image" class="w-full object-cover" />
    </div>
    <div class="web-text col-span-4">
      <h3 class="font-family1 text-very-dark text-4xl !mb-4">
        Webudvikling
      </h3>
      <p class="font-family3 text-very-dark text-lg">
        Den ene del af multimediedesign-verdenen for mig handler om at ideudvikle, designe og kode nye hjemmesider, samt vedligeholde og skabe nyt indhold på allerede eksisterende hjemmesider. Her har jeg kendskab til Figma, HTML, CSS, JavaScript, Vuejs, Tailwind, Github, Wordpress og en smule php. Undervejs på min uddannelse, har vi udviklet flere projekter, hvor vi har skulle bruge og vise vores evner indenfor disse områder. Et par eksempler kan ses på min portfolioside. 
      </p>
    </div>
  </div>

  <!-- Content Creation section -->
  <div class="content-creation-section grid grid-cols-12 gap-4">
    <div class="content-text col-span-4 col-start-2">
      <h3 class="font-family1 text-very-dark text-4xl !mb-4">
        Content Creation
      </h3>
      <p class="font-family3 text-very-dark text-lg">
        Den anden del af multimediedesign-verdenen for mig handler om at skabe fangende, æstetisk og engagerende content som alt lige fra logoer, plakater og visitkort til produktbilleder, reklamevideoer, animationer og meget mere.
        Her har jeg kendskab til Adobe programmerne: Indesign, Illustrator, Photoshop, Premiere Pro og After Effects, samt andre værktøjer som Canva, Canva Pro og Figjam. Eksempler på dette kan også ses på min portfolioside.
      </p>
    </div>
    <div class="col-span-7 mx-auto overflow-hidden h-125">
       <img src="../assets/somesamarbejder.png" alt="webudvikling Image" class="w-full object-contain" />
    </div>
  </div>

  <!-- Kontakt mig section -->
  <div class="kontakt-mig-section grid grid-cols-12">
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

<!-- Almindelig CSS Styles -------------------------------------------------------------------------------------------- -->

<style>
  .socials_wrapper img:hover {
    cursor: pointer;
  }

  .velkommen-section {
    margin-top: 10rem;
  }

  .velkommen-text-box {
    margin: 80px;
  }

  .webudviking-section {
    margin-top: 10rem;
  }

  .web-text {
    margin-left: 80px;
  }

  .content-creation-section {
    margin-top: 10rem;
  }

  .content-text {
    margin-right: 80px;
  }

  .kontakt-mig-section {
    margin-top: 10rem;
  }


  /* Media Queries for mobildesign ------------------------------------------------------------------------------------------------------------ */

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
      font-size: 1rem;
    }

    .relative h2 {
      font-size: 0.5rem;
    }


  /* Velkommen Section */
  .velkommen-section {
    height: auto; 
    padding: 1rem; 
    grid-template-columns: 1fr; 
    margin-top: 3rem;    }

  .velkommen-container {
    align-items: center; 
    height: auto; 
    padding: 1rem; 
    box-sizing: border-box; 
    width: 100%; 
    margin-top: 0
  }

  .velkommen-container img {
    display: none;
  }

  .velkommen-text-box {
    width: 100%; 
    padding: 1rem; 
    box-sizing: border-box; 
    margin: 0;
  }
  .velkommen-text-box h3 {
    font-size: 1rem; 
    margin: none; 
  }

  .velkommen-text-box p {
    font-size: 0.7rem; 
    margin: none; 
    width: 100%; 
  }


/* Webudvikling Section */

.webudviking-section {
    display: grid;
    grid-template-columns: 1fr; 
    grid-template-areas:
      "text"
      "image"; 
    gap: 2rem; 
    margin-top: 3rem;
  }

  .webudviking-section .col-span-7 {
    grid-area: image; 
    height: auto;
  }

  .webudviking-section .col-span-4 {
    grid-area: text; 
    margin-left: 0;  
    margin-left: 1.2rem;
    margin-right: 1.2rem;
  }

.web-text h3 {
  font-size: 1rem;
}

.web-text p {
  font-size: 0.7rem;
}



  /* Content Creation Section */
  .content-creation-section {
    display: grid;
    grid-template-columns: 1fr; 
    grid-template-areas:
      "text"
      "image"; 
    gap: 2rem; 
    margin-top: 3rem;
  }

  .content-creation-section .col-span-7 {
    grid-area: image; 
    height: auto;
  }

  .content-creation-section .col-span-4 {
    grid-area: text; 
    margin-left: 1.2rem;
    margin-right: 1.2rem;    
  }
  .content-creation-section img {
    width: 100%; 
    height: auto; 
  }

  .content-text h3 {
    font-size: 1rem; 
  }
  .content-text p {
    font-size: 0.7rem; 
  }

  /* Kontakt mig Section */
  .kontakt-mig-section {
    grid-template-columns: 1fr;
    gap: 1rem; 
    margin: 0 auto; 
    padding: 1rem; 
    margin-right: 2rem;
    margin-top: 3rem;
    height: auto;
    }

  .kontakt-mig-section > div {
    width: 100%; 
    margin: 0 auto; 
    padding: 1rem; 
    height: auto;
    padding: 1rem;
  }

  .kontakt-mig-section h3 {
    font-size: 1rem;
    text-align: center;
  }

  .kontakt-mig-section p {
    font-size: 0.7rem;
    text-align: center; 
  }

  .socials_wrapper {
    justify-content: center; 
    gap: 1rem; 
  }

  .socials_wrapper img {
    width: 20px; 
    height: 20px;
  }
  
  
}


</style>
