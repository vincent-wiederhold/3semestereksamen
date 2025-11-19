<script setup>
import Arrangement from '../components/Arrangement.vue';
import Carrusel from '../components/Carrusel.vue';
import FooterBottom from '../components/FooterBottom.vue';
import Navbar from '@/components/Navbar.vue';
</script>

<template>
  <Navbar/>
  <div class="herosection">
    <video src="../assets/dinahero.mp4" controls></video>
  </div>
  <div class="landingpagesection">
  <h1>DANSK KUNSTHÅNDVÆRK MED SJÆL</h1>
  <p>Hos Dina Vejling kan du gå på opdagelse i en verden af håndplukkede værker fra over 70 professionelle kunstnere. Find os i Brandts passage i Odense.</p>
  </div>
  <div class="aabningstidersection">
    <div class="grouping">
      <h1>ÅBNINGSTIDER</h1>
      <h4>Mandag - torsdag: kl. 11.00 - 17.30</h4>
      <h4>Fredag: kl. 11.00 - 18.00</h4>
      <h4>Lørdag: 10.30 - 14.00</h4>
      <h4>Søndag: Lukket</h4>
      <div class="kontaktoplysninger">
      <p>Dina Vejling - Dansk Kunsthåndværk</p><br>
      <p>Brandts passage 30, 5000 Odense C</p>
      <p>+45 28 30 14 05</p>
      </div>
      <button><font-awesome-icon icon="fa-solid fa-location-dot" class="fa-lg"/> FIND BUTIKKEN PÅ KORT</button>
    </div>
    <img src="../assets/dina_vejling_forside_1080x.webp" alt="">
  </div>


<div class="dividerimage">
<img src="../assets/markus-winkler-JZyHRn8Cq3k-unsplash.webp" alt="">
</div>
  <Arrangement/>
  <Carrusel/>
  <FooterBottom/>
</template>