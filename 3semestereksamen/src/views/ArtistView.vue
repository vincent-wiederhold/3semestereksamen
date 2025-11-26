<script setup>
import Navbar from '../components/Navbar.vue';
import FooterBottom from '../components/FooterBottom.vue';
import { ref } from 'vue';

const kunstner = ref([]);

const getKunstner = async () => {
    try {
        const res = await fetch('https://semestereksamen-85cb6-default-rtdb.europe-west1.firebasedatabase.app/kunstner.json', {
            method: 'GET',
        });
        const response = await res.json();
        kunstner.value = Object.values(response);
    } catch (error) {
        console.error(error);
    }
};

getKunstner();
</script>
<template>
    <Navbar />
    <div class="hero kunstner-hero">
    <h1 class="hero-text">Kunstnere</h1>
  </div>
<div class="section-wrapper">
    <h2>Hivlke ansigter gemmer sig bag værkerne</h2>
    <div class="artist">
        <li v-for="kunstnerData in kunstner" :key="kunstnerData">
        <p>{{ kunstnerData.Kunstnernavn }} - {{ kunstnerData.Profession }}</p>
        <p>{{ kunstnerData.Biografi }}</p>
        </li>
        <p>her kan der skiftes til andet indhold</p>
    </div>
</div>
    <FooterBottom />
</template>
