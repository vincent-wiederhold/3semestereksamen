<script setup>
import Arrangement from '../components/arrangement.vue';
import Carrusel from '../components/Carrusel.vue';
import FooterBottom from '../components/FooterBottom.vue';
</script>

<template>
  <div class="aabningstider">
    <h1>Åbningstider</h1>

    <h4> Mandag - torsdag: kl. 11.00 - 17.30 <br>
      Fredag: kl. 11.00 - 18.00 <br>
      Lørdag: 10.30 - 14.00 <br>
      Søndag: Lukket <br>
    </h4>
    <p>Dina Vejling - Dnask Kunsthåndværk</p>
    <br>
    <p>Brandts passage 30, 5000 Odense C <br>
      Tlf. +45 28 30 14 05
    </p>

    <img src="../assets/dina_vejling_forside_1080x.webp" alt="">
  </div>


<div class="dividerimage">
<img src="../assets/julelys.webp" alt="">
</div>
  <Arrangement/>
  <Carrusel/>
  <FooterBottom/>
</template>