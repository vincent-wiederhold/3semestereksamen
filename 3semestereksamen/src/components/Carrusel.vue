<script setup>
const getKunstner = () => {
    fetch('https://semestereksamen-85cb6-default-rtdb.europe-west1.firebasedatabase.app/kunstner.json',{
    method: 'GET'
})
    .then((response) => {
        return response.json();
    })
    .then((res) => {
        console.log(res);
    })
};

getKunstner();
</script>
<template>
    <div class="carruselsection">
        <h1>Populære kategorier</h1>
        <p>Se større udvalg af alle kategorier i butikken</p>
        <p><br><br><br>
            Her hentes dataerne
        </p>
    </div>
</template>
<style>
</style>