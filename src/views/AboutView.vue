<script setup>
import { onMounted, ref } from "vue";

const omMigSection = ref(null);

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

  if (omMigSection.value) observer.observe(omMigSection.value);
});
</script>

<template>
  <main class="overflow-hidden">

<!-- Hero Section -->
<div class="relative w-full h-200 overflow-hidden">
  <!-- Hero Image -->
  <img src="../assets/mig.jpg" alt="Home Hero Image" class="absolute top-0 left-0 w-full h-200 object-cover" />
      
    <!-- Centered Text -->
    <div class="absolute inset-0 flex flex-col items-center justify-center text-center">
        <h1 class="font-family1 text-butter-yellow text-5xl !mb-4">
          OM MIG
        </h1>
    </div>
</div>

<!-- Om mig section -->
<div class="om-mig-section grid grid-cols-12 h-150 opacity-0 translate-x-20 transition-all duration-700"ref="omMigSection">
  <div class="om-mig-container col-span-8 col-start-3 h-150 bg-very-light-grey flex items-center">
    <div class="om-mig-text-box">
      <h3 class="font-family1 text-very-dark text-4xl">
        Hvem er jeg?
      </h3>
      <p class="font-family3 text-very-dark text-lg w-3/4 !mt-4">
        Mit navn er Mia, og jeg er en kreativ person med en stor interresse for at skabe æstetisk indhold og udvikle hjemmesider. 
        Jeg har altid haft en interesse for design og teknologi, og derfor valgte jeg at tage en uddannelse som multimediedesigner. 
        Jeg er perfektionist og elsker at arbejde med detaljer, hvilket hjælper mig utrolig meget indenfor både design og webudvikling.
      </p>
      <p class="font-family3 text-very-dark text-lg w-3/4 !mt-4">
        I min fritid elsker jeg at være kreativ, og jeg bruger meget tid på at lave indhold til sociale medier, samt at tage billeder og redigere videoer.
        Derudover elsker jeg at være aktiv, og jeg bruger meget tid på at træne og være ude i naturen, samt at bruge tid med mine venner og familie. 
        På denne side kan du læse mere om mig som person, se mit video CV herunder, samt mit CV og visitkort.
      </p>
    </div>
    <!-- CV & Visitkort -->
    <div class="cv-businesscard-section flex flex-col items-center justify-center">
      <a 
        href="/assets/CV.pdf" 
        target="_blank" 
        rel="noopener noreferrer" 
        class="cv-button bg-very-grey text-butter-yellow font-family1 w-30 h-20 flex items-center justify-center">
        CV
      </a>
      <a 
        href="/assets/Businesscard.pdf" 
        target="_blank" 
        rel="noopener noreferrer" 
        class="bg-very-grey text-butter-yellow font-family1 w-30 h-20 flex items-center justify-center">
        Visitkort
      </a>
    </div>
  </div>
</div>

    <!-- Video cv section -->
    <div class="video-cv-section flex justify-center items-center bg-very-light-grey h-150">
      <iframe width="800" height="450" src="https://www.youtube.com/embed/lAhP_2eKS8I?si=xJEzl8vM0EBMGp7K" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
    </div>


<div class="personal-section bg-very-light-grey h-20 flex items-center">
  <h3 class="font-family1 text-very-dark text-4xl">
    Og så til det personlige!
  </h3>
</div>

<!-- Collage section 1 -->

<div class="collage-section-text flex flex-col">
    <h3 class="font-family1 text-very-dark text-4xl !mb-4">
      Jeg elsker at rejse, og tage flotte billeder undervejs!
    </h3>
    <p class="font-family3 text-lg text-very-dark w-1/2">
      Jeg elsker at rejse – følelsen af at være på vej et nyt sted hen, hvor alt føles friskt og uopdaget. Det er som om verden åbner sig lidt mere, hver gang jeg pakker min taske og tager afsted. Undervejs har kameraet altid en fast plads i hånden eller lommen. Det handler ikke bare om at tage billeder, men om at fange stemninger, farver og øjeblikke, som ellers ville flyve forbi. Små detaljer, gadeliv, landskaber og smil – det hele bliver til minder, jeg kan vende tilbage til igen og igen.
    </p>
</div>

<div class="photo-collage grid grid-cols-12 gap-4">
  <!-- First Image -->
  <div class="col-span-4">
    <img src="../assets/collage1.jpg" alt="Photo 1" class="w-full h-200 object-cover" />
  </div>
  <!-- Second Image -->
  <div class="col-span-4">
    <img src="../assets/collage2.jpg" alt="Photo 2" class="w-full h-200 object-cover" />
  </div>
  <!-- Third Image -->
  <div class="col-span-4">
    <img src="../assets/collage3.jpg" alt="Photo 3" class="w-full h-200 object-cover" />
  </div>
</div>


<!-- Collage section 2 -->

<div class="collage-section-text flex flex-col">
    <h3 class="font-family1 text-very-dark text-4xl !mb-4">
      Ude godt men hjemme bedst!
    </h3>
    <p class="font-family3 text-lg text-very-dark w-1/2">
      Selvom jeg elsker at rejse, så elsker jeg også at være hjemme og at indrette mit hjem – det føles som en kreativ proces, hvor hver ting får sin plads og sin betydning. Der er noget roligt og tilfredsstillende ved at skabe et rum, der føles rart at være i. At rydde op og skabe orden giver ikke kun visuel ro, men også mental klarhed. Jeg nyder at finde balance mellem funktion og æstetik, og det giver mig glæde, når hjemmet føles både personligt, indbydende og harmonisk.
    </p>
  </div>

  <div class="photo-collage grid grid-cols-12 gap-4">
  <!-- First Image -->
  <div class="col-span-4">
    <img src="../assets/spisestue.jpg" alt="Photo 1" class="w-full h-200 object-cover" />
  </div>
  <!-- Second Image -->
  <div class="col-span-4">
    <img src="../assets/sofastue.jpg" alt="Photo 2" class="w-full h-200 object-cover" />
  </div>
  <!-- Third Image -->
  <div class="col-span-4">
    <img src="../assets/køkken.jpg" alt="Photo 3" class="w-full h-200 object-cover" />
  </div>
</div>

<!-- Collage section 3 -->

<div class="collage-section-text flex flex-col">
    <h3 class="font-family1 text-very-dark text-4xl !mb-4">
      Jeg nyder at være aktiv!
    </h3>
    <p class="font-family3 text-lg text-very-dark w-1/2">
      Jeg bruger også meget tid på at være aktiv – både i fitnesscentret og ude i naturen. Der er noget stærkt ved følelsen af at bruge kroppen og mærke energien strømme. I fitness elsker jeg strukturen og fremgangen, mens naturen giver frihed, frisk luft og ro i sindet. Det er to vidt forskellige steder, men begge giver mig overskud, styrke og glæde. At bevæge sig er ikke bare træning – det er en måde at være til stede i nuet på.
    </p>
</div>

<div class="photo-collage grid grid-cols-12 gap-4">
  <!-- First Image -->
  <div class="col-span-4">
    <img src="../assets/natur.jpg" alt="Photo 1" class="w-full h-200 object-cover" />
  </div>
  <!-- Second Image -->
  <div class="col-span-4">
    <img src="../assets/fitness.jpg" alt="Photo 2" class="w-full h-200 object-cover" />
  </div>
  <!-- Third Image -->
  <div class="col-span-4">
    <img src="../assets/løb.jpg" alt="Photo 3" class="w-full h-200 object-cover" />
  </div>
</div>

<!-- Collage section 4 -->

<div class="collage-section-text flex flex-col">
    <h3 class="font-family1 text-very-dark text-4xl !mb-4">
      Jeg udtrykker mig gennem mit tøj og min stil!
    </h3>
    <p class="font-family3 text-lg text-very-dark w-1/2">
      Jeg elsker at udtrykke mig gennem mit tøj og min stil. Det er en måde at vise, hvem jeg er, uden at sige et ord. Farver, snit og detaljer fortæller små historier om mit humør, min kreativitet og min personlighed. Nogle dage er det klassisk og enkelt, andre dage legende og modigt – og begge dele føles lige rigtige. Stil er for mig ikke bare mode, men en forlængelse af mig selv.
    </p>
</div>

<div class="photo-collage grid grid-cols-12 gap-4">
  <!-- First Image -->
  <div class="col-span-4">
    <img src="../assets/tøj2.jpg" alt="Photo 1" class="w-full h-200 object-cover" />
  </div>
  <!-- Second Image -->
  <div class="col-span-4">
    <img src="../assets/tøj1.jpg" alt="Photo 2" class="w-full h-200 object-cover" />
  </div>
  <!-- Third Image -->
  <div class="last-image col-span-4">
    <img src="../assets/tøj3.jpg" alt="Photo 3" class="w-full h-200 object-cover" />
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


<!-- Almindelig css styles -------------------------------------------------------------------------------------------------------------------- -->

<style>

.om-mig-section {
  margin-top: 10rem;
}

.om-mig-text-box {
  margin-left: 80px;
}

.cv-businesscard-section {
  margin-right: 80px;
}

.cv-button {
  margin-bottom: 3rem;
}

.video-cv-section {
  margin-top: 10rem;
}

.personal-section {
  margin-top: 10rem;
}

.personal-section h3 {
  margin-left: 80px;
}

.collage-section-text {
  margin-left: 80px;
  margin-top: 5rem;
}

.photo-collage {
  margin-top: 5rem;
  margin-bottom: 10rem;
}

.kontakt-mig-section {
  margin-top: 10rem;
}



  /* Media Queries for mobildesign ------------------------------------------------------------------------------------------------------------ */


@media (max-width: 768px) {

/* Om mig section */

.om-mig-section {
  height: auto; 
  padding: 1rem; 
  grid-template-columns: 1fr; 
  margin-top: 3rem; 
}

.om-mig-container {
  align-items: center; 
  height: auto; 
  padding: 1rem; 
  box-sizing: border-box; 
  width: 100%; 
  margin-top: 0;
  flex-direction: column;
}

.om-mig-container img {
  display: none; 
}

.om-mig-text-box {
  width: 100%; 
  padding: 1rem; 
  box-sizing: border-box; 
  margin: 0;
}

.om-mig-text-box h3 {
  font-size: 1rem; 
  margin: 0; 
}

.om-mig-text-box p {
  font-size: 0.7rem; 
  margin: 0; 
  width: 100%; 
  margin-bottom: 1rem;
}

.cv-businesscard-section {
  display: flex;
  flex-direction: row;
  justify-content: center;
  align-items: center;
  margin-right: 0;
}

.cv-businesscard-section a {
  width: 5rem;
  height: 2rem;
  font-size: 0.7rem;
  display: flex;
  justify-content: center;
  align-items: center;
  margin-bottom: 2em;
}


.cv-button {
  margin-bottom: 0;
  margin-right: 3rem;
}

.video-cv-section {
  margin-top: 3rem;
  height: 200px;
}
  
.video-cv-section iframe {
  width: 100%;
  height: auto;
}

.personal-section {
  margin-top: 3rem;
  height: 45px;
}

.personal-section h3 {
  font-size: 1rem;
  margin-left: 1rem;
}

.collage-section-text {
  margin-left: 1rem;
  margin-top: 2rem;
  width: 100%;
}

.collage-section-text h3 {
  font-size: 1rem;
  margin-bottom: 0.5rem;
  width: 100%;
}

.collage-section-text p {
  font-size: 0.7rem;
  margin-bottom: 1rem;
  width: 90%;
}

.photo-collage {
    display: grid;
    grid-template-columns: 1fr; 
    gap: 1rem; 
    margin-top: 1rem; 
    margin-bottom: 5rem;
  }

  .photo-collage img {
    width: 100%; 
    height: auto; 
    object-fit: cover;
  }

  .kontakt-mig-section {
    margin-top: 3rem
  }


}







</style>
