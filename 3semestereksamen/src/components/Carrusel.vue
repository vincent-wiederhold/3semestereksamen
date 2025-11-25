<script setup>
import {ref } from 'vue';

const kunstner = ref([]);

const getKunstner = async () => {
    try{
        const res = await fetch('https://semestereksamen-85cb6-default-rtdb.europe-west1.firebasedatabase.app/kunstner.json',{
        method: 'GET',
        });

    const response = await res.json();

    console.log('Firebase Response', response);

    kunstner.value = Object.values(response);

    console.log(response)
    console.log('Kunstner Data:', kunstner.value);
    } catch(error) {
        console.error(error);
    }
};

getKunstner();
</script>
<template>
    <div class="carruselsection">
        <h1>Populære Kunstnere</h1>
        <p>Kom ned i butikken og spørg ind til kunstnerne og deres værker eller læs mere ved at trykke på dem</p>
        <div class="kunstnere">
            <li v-for="(kunstnerData, index) in kunstner" :key="index">
                <p>{{ kunstnerData.Kunstnernavn }}</p>
                <p>{{ kunstnerData.Profession }}</p>
            </li>
        </div>
    </div>
</template>
<style>
</style>