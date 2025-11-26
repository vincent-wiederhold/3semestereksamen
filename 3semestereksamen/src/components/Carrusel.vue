<script setup>
import { computed, ref} from 'vue';

const kunstner = ref([]);
const startIndex = ref(0)
const kunstnerLoaded = ref(false)

const getKunstner = async () => {
    if (kunstnerLoaded.value) return;
    try{
        const res = await fetch('https://semestereksamen-85cb6-default-rtdb.europe-west1.firebasedatabase.app/kunstner.json',{
        method: 'GET',
        });

    const response = await res.json();

    console.log('Firebase Response', response);

    kunstner.value = Object.values(response);

    kunstnerLoaded.value = true;
 
    console.log(response)
    console.log('Kunstner Data:', kunstner.value);
    } catch(error) {
        console.error(error);
    }
};

getKunstner();

const next = () => {
    startIndex.value++;
    if( startIndex.value >= kunstner.value.length) {
        startIndex.value = 0;
    }
};

const visibleKunstnere = computed(() => {
    const result = [];
    for (let i = 0; i< 3; i++){
        let visibleIndex = startIndex.value + i;
        if( visibleIndex >= kunstner.value.length) {
            visibleIndex = visibleIndex - kunstner.value.length;
        }
        result.push(kunstner.value[visibleIndex]);
    }
    return result;
});

const prev = () => {
    startIndex.value--;
    if (startIndex.value< 0) {
        startIndex.value = kunstner.value.length -1;
    }
};

</script>
<template>
    <div class="carruselsection">
        <h1>Populære Kunstnere</h1>
        <p>Kom ned i butikken og spørg ind til kunstnerne og deres værker eller læs mere ved at trykke på dem</p>
        <div class="kunstnere">
            <ul v-if="kunstner.length > 0">
                <button v-on:click="prev"><</button>
                <li v-for="kunstnerData in visibleKunstnere" :key="kunstnerData">
                    <p>{{ kunstnerData.Kunstnernavn }}</p>
                    <p>{{ kunstnerData.Profession }}</p>
                </li>
                <button v-on:click="next">></button>
            </ul>
        </div>
    </div>
</template>
<style>
</style>