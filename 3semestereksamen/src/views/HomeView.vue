<script setup>
import Arrangement from '../components/arrangement.vue';
import Carrusel from '../components/Carrusel.vue';
import FooterBottom from '../components/FooterBottom.vue';
</script>

<template>
  <div class="section">
    <h1>DIT ONLINEKATALOG FOR DET DANSKE KUNSTHÅNDVÆRKSHJEM</h1>
    <p>Dina Vejling sælger og udstiller 70 kunstneres moderne og danske kunsthåndværk. De er professionelt udannet og de fleste på en af vores designskoler i Danmark. Enkelte kunstnere er fra kunstakademiet eller tilsvarende skoler i udlandet.   Indehaver Dina Vejling har et bredt kendskab til kunstnerne og deres værker, da hun prioriterer at besøge dem på værkstederne rundt om i landet og udvælger det, som hun anser for det bedste, og bringer det hjem til Odense. Dette katalog er et lille overblik over, hvad vi har i butikken, men der er meget mere nede i butikken.</p>
  </div>
  <div class="section">
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