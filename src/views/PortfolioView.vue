<script setup>
import { onMounted, ref } from "vue";

const portfolioSection = ref(null);

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

  if (portfolioSection.value) observer.observe(portfolioSection.value);
});
</script>

<template>
  <main class="overflow-hidden">
    <!-- Hero Section -->
    <div class="relative w-full h-200 overflow-hidden">
      <img src="../assets/portfoliohero.png" alt="Home Hero Image" class="absolute top-0 left-0 w-full h-200 object-cover" /> 
      <div class="absolute inset-0 flex flex-col items-center justify-center text-center">
        <h1 class="font-family1 text-very-dark text-5xl !mb-4">
          PORTFOLIO
        </h1>
      </div>
    </div>

<!-- Portfolio section -->
<div class="portfolio-section grid grid-cols-12 h-125 opacity-0 translate-x-20 transition-all duration-700" ref="portfolioSection">
  <div class="portfolio-container col-span-8 col-start-3 h-125 bg-very-light-grey flex items-center">
    <div class="portfolio-text-box">
      <h3 class="font-family1 text-very-dark text-4xl !mb-4">
        Hvad kan man egentlig som multimediedesigner?
      </h3>
      <p class="font-family3 text-very-dark text-lg w-2/3">
        På denne side kan du læse om nogle af de projekter jeg har lavet under min uddannelse som multimediedesigner, hvilket forhåbenligt kan give et indblik i de kompetencer jeg har tilegnet mig, og stadig arbejder hver dag på at forbedre!
        Derudover kan du også læse om noget af det arbejde jeg har lavet udenfor skolen som SoMe content creator, hvor jeg har arbejdet med at skabe indhold til sociale medier for forskellige brands.
      </p>
    </div>
    <img src="../assets/pil.svg" alt="welcome Image" class="w-1/3 justify-self-end !mb-1 !pr-20 h-50" />
  </div>
</div>

<!-- Hotel website section -->
<div class="hotel-website-section grid grid-cols-12 gap-4">
  <div class="col-span-7 mx-auto overflow-hidden h-125">
    <img src="../assets/hotelsite.png" alt="webudvikling Image" class="w-full object-cover" />
  </div>
  <div class="hotel-text-box col-span-4">
    <h3 class="font-family1 text-very-dark text-4xl !mb-4">
      Hotel Hjemmeside
    </h3>
    <p class="font-family3 text-very-dark text-lg">
      For at lære Wordpress at kende, samt projektstyringsmetoden SCRUM, fik vi til opgave at lave en hotel hjemmeside, med forskellige user story krav, hvor vi undervejs i processen hver især havde forskellige roller i gruppen, præcis som man ville have på en arbejdsplads.
    </p>
  </div>
</div>
    
    
<!-- Swim run event section -->
<div class="event-section grid grid-cols-12 gap-4">
  <div class="event-text-box col-span-4 col-start-2">
    <h3 class="font-family1 text-very-dark text-4xl !mb-4">
      Swim Run Event
    </h3>
    <p class="font-family3 text-very-dark text-lg">
    Vi fik til opgave at finde på et nyt event til Esbjerg, for at trække folk til udefra. Vi valgte at foreslå et Swim Run event, hvor vi efter at have undersøgt statistikker og segmenteret, fik taget billeder, filmet en reklamevideo, lavet en Instagram, en plakat og en content kalender for planen af de forskellige opslag.
    </p>
  </div>
  <div class="col-span-7 mx-auto overflow-hidden h-125 border-2">
    <img src="../assets/swimrun.png" alt="webudvikling Image" class="w-full object-contain" />
  </div>
</div>
    



<!-- Recipe Webside section -->
<div class="recipe-website-section grid grid-cols-12 gap-4">
  <div class="col-span-7 mx-auto overflow-hidden h-125">
    <img src="../assets/opskrifthjemmeside.png" alt="webudvikling Image" class="w-full object-cover" />
  </div>
  <div class="recipe-text-box col-span-4">
    <h3 class="font-family1 text-very-dark text-4xl !mb-4">
      Opskrift Hjemmeside
    </h3>
    <p class="font-family3 text-very-dark text-lg">
      Et af vores første projekter på uddannelsen var, at designe en opskrifts-hjemmeside i Figma, samt kode den i HTML og CSS. 
    </p>
  </div>
</div>

<!-- Plastic project section -->
<div class="plastic-project-section grid grid-cols-12 gap-4">
  <div class="plastic-project-text-box col-span-4 col-start-2">
    <h3 class="font-family1 text-very-dark text-4xl !mb-4">
      Plastik Projekt
    </h3>
    <p class="font-family3 text-very-dark text-lg">
      Til det afsluttende semesterprojekt på 1. semester var opgaven, at skabe en hjemmeside og alt hvad vi vurderede hørte til, for at skabe budskabet om en global plastiktraktat. Målet var at få folk til at skrive under, samt gøre opmærksom på situationen. Her lavede vi er masse research og indsamlede data for at bakke vores valg af målgruppe og design op. Udover hjemmesiden lavede vi en Instagram-konto, et mood board, en plakat, et logo, en reklamevideo og et design brief. På denne måde fik vi under dette projekt brugt alle de programmer og erfaringer vi fik med under hele 1. semester.
    </p>
  </div>
  <div class="col-span-7 mx-auto overflow-hidden h-125">
    <img src="../assets/Plastic website.png" alt="webudvikling Image" class="w-full object-contain" />
  </div>
</div>

<!-- Promo video section -->
<div class="promo-video-section grid grid-cols-12 gap-4">
  <div class="col-span-7 mx-auto overflow-hidden h-125">
    <img src="../assets/reklamevideo.png" alt="webudvikling Image" class="w-full object-cover" />
  </div>
  <div class="promo-text-box col-span-4">
    <h3 class="font-family1 text-very-dark text-4xl !mb-4">
      Reklame Video 
    </h3>
    <p class="font-family3 text-very-dark text-lg">
      På 2. semester har vi arbejdet meget med videoredigering, og dette har vi blandt andet brugt til at lave en reklamevideo for multimediedesign-uddannelsen. Videoen er redigeret i både Premiere, After Effects, og Canva.
    </p>
  </div>
</div>

<!-- Cafe app section -->
<div class="cafe-app-section grid grid-cols-12 gap-4">
  <div class="cafe-text-box col-span-4 col-start-2">
    <h3 class="font-family1 text-very-dark text-4xl !mb-4">
      Cafe App
    </h3>
    <p class="font-family3 text-very-dark text-lg">
      I faget User Experience, har vi under hele 2. semester skulle designe en valgfri app, med fokus på at gøre den brugervenlig, intuitiv og æstetisk. Vi valgte at designe en app for en cafe, der gør det muligt for kunder at forudbestille, samle loyalitetspoint, se menuen, kontaktinfo/åbningstider og billeder af den hyggelige atmosfære. 
    </p>
  </div>
  <div class="col-span-7 mx-auto overflow-hidden h-125 border-1">
    <img src="../assets/cafeapp.png" alt="webudvikling Image" class="w-full object-contain" />
  </div>
</div>

<!-- Velkomst projekt -->
<div class="velkomst-projekt-section grid grid-cols-12 gap-4">
  <div class="col-span-7 mx-auto overflow-hidden h-125">
    <img src="../assets/velkomstprojekt.png" alt="webudvikling Image" class="w-full object-cover" />
  </div>
  <div class="velkomst-text-box col-span-4">
    <h3 class="font-family1 text-very-dark text-4xl !mb-4">
      Velkomst Projekt 
    </h3>
    <p class="font-family3 text-very-dark text-lg">
      “Velkommen til” projektet gik ud på, at lave en flyer for et valgfrit område i Esbjerg eller omegn. Her valgte vi Sjelborgdalen, og lavede en virtuel flyer i Indesign med flotte billede, en stemningsvideo, information om området samt et kort lavet i illustrator. 
    </p>
  </div>
</div>

<!-- So me section -->
<div class="so-me-section grid grid-cols-12 gap-4">
  <div class="so-me-text-box col-span-4 col-start-2">
    <h3 class="font-family1 text-very-dark text-4xl !mb-4">
      SoMe Samarbejder
    </h3>
    <p class="font-family3 text-very-dark text-lg">
      Udover de mange skoleprojekter har jeg lavet lidt forskelligt arbejde ved siden af for en masse brands på sociale medier. Her har jeg lavet produktbilleder og reklamevideoer til brug for deres hjemmesider og sociale medier. Jeg har lavet content for brands som: Skoringen, I Can I Will, Arla, Logitec, Reshoppit, Hatting, Studio Z smykker, Sistie smykker samt flere. Det meste content kan findes på min Instagram.
    </p>
  </div>
  <div class="col-span-7 mx-auto overflow-hidden h-125">
    <img src="../assets/somesamarbejder.png" alt="webudvikling Image" class="w-full object-contain" />
  </div>
</div>

  </main>
</template>


<!-- Almindelig css styles -------------------------------------------------------------------------------------------------------------------- -->
<style>

.portfolio-section {
    margin-top: 10rem;
  }

  .portfolio-text-box {
    margin: 80px;
  }

  .hotel-website-section{
    margin-top: 10rem;
  }

  .hotel-text-box {
    margin-left: 80px;
  }

  .event-section {
    margin-top: 10rem;
  }

  .event-text-box {
    margin-right: 80px;
  }

  .recipe-website-section {
    margin-top: 10rem;
  }

  .recipe-text-box {
    margin-left: 80px;
  }

  .plastic-project-section {
    margin-top: 10rem;
  }

  .plastic-project-text-box {
    margin-right: 80px;
  }

  .promo-video-section {
    margin-top: 10rem;
  }

  .promo-text-box {
    margin-left: 80px;
  }

  .cafe-app-section {
    margin-top: 10rem;
  }

  .cafe-text-box {
    margin-right: 80px;
  }

  .velkomst-projekt-section {
    margin-top: 10rem;
  }

  .velkomst-text-box {
    margin-left: 80px;
  }

  .so-me-section {
    margin-top: 10rem;
  }

  .so-me-text-box {
    margin-right: 80px;
  }





  /* Media Queries for mobildesign ------------------------------------------------------------------------------------------------------------ */


@media (max-width: 768px) {
/* Portfolio */

.relative h1 {
  padding-top: 1rem;
}

.portfolio-section {
  height: auto; 
  padding: 1rem; 
  grid-template-columns: 1fr; 
  margin-top: 3rem; 
}

.portfolio-container {
  align-items: center; 
  height: auto; 
  padding: 1rem; 
  box-sizing: border-box; 
  width: 100%; 
  margin-top: 0;
}

.portfolio-container img {
  display: none; 
}

.portfolio-text-box {
  width: 100%; 
  padding: 1rem; 
  box-sizing: border-box; 
  margin: 0;
}

.portfolio-text-box h3 {
  font-size: 1rem; 
  margin: 0; 
}

.portfolio-text-box p {
  font-size: 0.7rem; 
  margin: 0; 
  width: 100%; 
}

/* Hotel Website Section */
.hotel-website-section {
  display: grid;
  grid-template-columns: 1fr; 
  grid-template-areas:
    "text"
    "image"; 
  gap: 2rem; 
  margin-top: 3rem;
}

.hotel-website-section .col-span-7 {
  grid-area: image; 
  height: auto;
}

.hotel-website-section .col-span-4 {
  grid-area: text; 
  margin-left: 1.2rem;  
  margin-right: 1.2rem;
}

.hotel-text-box {
  margin: 0;
}
.hotel-text-box h3 {
  font-size: 1rem;
}

.hotel-text-box p {
  font-size: 0.7rem;
}

/* Event Section */
.event-section {
  display: grid;
  grid-template-columns: 1fr; 
  grid-template-areas:
    "text"
    "image"; 
  gap: 2rem; 
  margin-top: 3rem;
}

.event-section .col-span-7 {
  grid-area: image; 
  height: auto;
}

.event-section .col-span-4 {
  grid-area: text; 
  margin-left: 1.2rem;
  margin-right: 1.2rem;    
}

.event-section img {
  width: 100%; 
  height: auto; 
}

.event-text-box {
  margin: 0;
}

.event-text-box h3 {
  font-size: 1rem; 
}

.event-text-box p {
  font-size: 0.7rem; 
}

/* Recipe Website Section */
.recipe-website-section {
  display: grid;
  grid-template-columns: 1fr; 
  grid-template-areas:
    "text"
    "image"; 
  gap: 2rem; 
  margin-top: 3rem;
}

.recipe-website-section .col-span-7 {
  grid-area: image; 
  height: auto;
}

.recipe-website-section .col-span-4 {
  grid-area: text; 
  margin-left: 1.2rem;  
  margin-right: 1.2rem;
}

.recipe-text-box {
  margin: 0;
}

.recipe-text-box h3 {
  font-size: 1rem;
}

.recipe-text-box p {
  font-size: 0.7rem;
}

/* Plastic Project Section */

.plastic-project-section {
  display: grid;
  grid-template-columns: 1fr; 
  grid-template-areas:
    "text"
    "image"; 
  gap: 2rem; 
  margin-top: 3rem;
}

.plastic-project-section .col-span-7 {
  grid-area: image; 
  height: auto;
}

.plastic-project-section .col-span-4 {
  grid-area: text; 
  margin-left: 1.2rem;
  margin-right: 1.2rem;    
}

.plastic-project-section img {
  width: 100%; 
  height: auto; 
}

.plastic-project-text-box {
  margin: 0;
}

.plastic-project-text-box h3 {
  font-size: 1rem; 
}

.plastic-project-text-box p {
  font-size: 0.7rem; 
}

/* Promo Video Section */

.promo-video-section {
  display: grid;
  grid-template-columns: 1fr; 
  grid-template-areas:
    "text"
    "image"; 
  gap: 2rem; 
  margin-top: 3rem;
}

.promo-video-section .col-span-7 {
  grid-area: image; 
  height: auto;
}

.promo-video-section .col-span-4 {
  grid-area: text; 
  margin-left: 1.2rem;  
  margin-right: 1.2rem;
}

.promo-text-box {
  margin: 0;
}

.promo-text-box h3 {
  font-size: 1rem;
}

.promo-text-box p {
  font-size: 0.7rem;
}

/* Cafe App Section */

.cafe-app-section {
  display: grid;
  grid-template-columns: 1fr; 
  grid-template-areas:
    "text"
    "image"; 
  gap: 2rem; 
  margin-top: 3rem;
}

.cafe-app-section .col-span-7 {
  grid-area: image; 
  height: auto;
}

.cafe-app-section .col-span-4 {
  grid-area: text; 
  margin-left: 1.2rem;
  margin-right: 1.2rem;    
}

.cafe-app-section img {
  width: 100%; 
  height: auto; 
}

.cafe-text-box {
  margin: 0;
}

.cafe-text-box h3 {
  font-size: 1rem; 
}

.cafe-text-box p {
  font-size: 0.7rem; 
}

/* Velkomst Projekt Section */

.velkomst-projekt-section {
  display: grid;
  grid-template-columns: 1fr; 
  grid-template-areas:
    "text"
    "image"; 
  gap: 2rem; 
  margin-top: 3rem;
}

.velkomst-projekt-section .col-span-7 {
  grid-area: image; 
  height: auto;
}

.velkomst-projekt-section .col-span-4 {
  grid-area: text; 
  margin-left: 1.2rem;  
  margin-right: 1.2rem;
}

.velkomst-text-box {
  margin: 0;
}

.velkomst-text-box h3 {
  font-size: 1rem;
}

.velkomst-text-box p {
  font-size: 0.7rem;
}

/* SoMe Section */

.so-me-section {
  display: grid;
  grid-template-columns: 1fr; 
  grid-template-areas:
    "text"
    "image"; 
  gap: 2rem; 
  margin-top: 3rem;
}

.so-me-section .col-span-7 {
  grid-area: image; 
  height: auto;
}

.so-me-section .col-span-4 {
  grid-area: text; 
  margin-left: 1.2rem;
  margin-right: 1.2rem;    
}

.so-me-section img {
  width: 100%; 
  height: auto; 
}

.so-me-text-box {
  margin: 0;
}

.so-me-text-box h3 {
  font-size: 1rem; 
}

.so-me-text-box p {
  font-size: 0.7rem; 
}


}

</style>
