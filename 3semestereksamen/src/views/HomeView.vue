<script setup>
import Arrangement from '../components/Arrangement.vue';
import Carrusel from '../components/Carrusel.vue';
import FooterBottom from '../components/FooterBottom.vue';
import Navbar from '@/components/Navbar.vue';

const playPause = document.getElementById("play-pause");
// Hide the default controls
video.controls = false;
// Display the user defined video controls
videoControls.setAttribute("data-state", "visible");
function changeButtonState(type) {
  if (type === "play-pause") {
    // Play/Pause button
    if (video.paused || video.ended) {
      playPause.setAttribute("data-state", "play");
    } else {
      playPause.setAttribute("data-state", "pause");
    }
  } 
}
video.addEventListener("play", () => {
  changeButtonState("play-pause");
});

video.addEventListener("pause", () => {
  changeButtonState("play-pause");
});

stop.addEventListener("click", (e) => {
  video.pause();
  video.currentTime = 0;
  progress.value = 0;

  // Update the play/pause button's 'data-state' which allows the
  // correct button image to be set via CSS
  changeButtonState("play-pause");
});

playPause.addEventListener("click", (e) => {
  if (video.paused || video.ended) {
    video.play();
  } else {
    video.pause();
  }
});
</script>

<template>
  <Navbar/>

<figure id="videoContainer">
  <video id="video" controls> <source src="../assets/dinahero.mp4" type="video/mp4"/> </video>
  <div id="video-controls" class="controls" data-state="hidden">
    <button id="play-pause" type="button" data-state="play">Play/Pause</button>
  </div>
</figure>

  <div class="herosection">
    <video src="../assets/dinahero.mp4" controls autoplay loop></video>
    <div class="controls">
      <button>Play/Pause</button>

    </div>
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