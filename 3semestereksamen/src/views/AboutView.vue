<script setup>
import Navbar from '@/components/Navbar.vue';
import FooterBottom from '@/components/FooterBottom.vue';
import ImageBorderLeft from '@/components/ImageBorderLeft.vue';
import butikIndenfor from '@/assets/images/butik/dinavejling-butik-indenfor.jpg';
</script>

<template>
  <Navbar />
  <div class="hero">
    <h1>Om os</h1>
  </div>

  <div class="section-wrapper">
    <h2 class="heading">HVEM ER VI?</h2>
    <p class="paragraf">Hos Dina Vejling sælger og udstiller vi moderne dansk kunsthåndværk af mere end 70 kunstnere. 
      Vi har alt fra keramik og glas til smykker og snedkeri, og så har vi også et mindre udvalg af 
      sølvtøj, tekstiler og grafiske kunstværker. Indehaver Dina Vejling har et bredt kendskab til 
      kunstnerne og deres værker, da hun tager ud og besøger dem på deres værksteder rundt om i landet. 
      Her bringer hun de bedste værker med hjem til Odense, så du kan gå på opdagelse i en verden af 
      ægte kunsthåndværk.</p>
    <p class="paragraf">Butikken blev etableret i 2005 og ligger i de historiske haller i den tidligere Brandts Klædefabrik. 
      Området har bevaret sit autentiske udtryk, hvilket man fornemmer i de forretninger og caféer, der 
      befinder sig her. Man fornemmer næsten den fabrikation, der fandt sted i butikslokalerne for ikke så 
      mange år siden. På den måde forbinder Dina Vejling - Dansk Kunsthåndværk sig til det historiske, 
      hvilket er noget, som vi er meget stolte af.</p>
    <div class="image-wrapper left">
      <ImageBorderLeft :src="butikIndenfor" alt=""/>
    </div>
  </div>

  <div class="section-wrapper">

  </div>
  




  <FooterBottom />
</template>

<style>
</style>
