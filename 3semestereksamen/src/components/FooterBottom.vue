<script setup>
</script>
<template>
    <footer>
        <div class="footercontent">
            <h4>Åbningstider</h4>
            <ul>
                <li>Mandag - torsdag: kl. 11.00 - 17.30</li>
                <li>Fredag: kl. 11.00 - 18.00</li>
                <li>Sødag: Lukket</li>
            </ul>
            <h4>Konkaktoplysinger</h4>
            <ul>
                <li><font-awesome-icon icon="fa-solid fa-location-dot" class="fa-lg" /> Brandtspassage 30, 5000 Odense C</li>
                <li><font-awesome-icon icon="fa-solid fa-envelope" class="fa-lg" /> info@dinavejling.dk</li>
                <li><font-awesome-icon icon="fa-solid fa-phone" class="fa-lg"/> +45 28 30 14 05</li>
            </ul>
            <h4>Informationer</h4>
            <ul>
                <li>Om Dina Vejling</li>
                <li>Handelsbetingelser</li>
                <li>Galleri Rummet</li>
                <li>Arrengementer</li>
                <li>Kunstnere</li>
            </ul>
        
            <h4>Følg Dina Vejling</h4>
            <div class="some">
                <font-awesome-icon icon="fa-brands fa-instagram" class="fa-4x"/>
                <font-awesome-icon icon="fa-brands fa-square-facebook" class="fa-4x"/>
            </div>
            <img src="../assets/dinavejling.svg" alt="" class="logo">
            
        </div>
        <div class="footerbanner">
            <p>@ 2025 Dina Vejling - Dansk Kunsthåndværk</p>
            <p>Drevet af Dina Vejling</p>
        </div>
    </footer>
</template>

<style>
*{
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    font-family: "Quicksand", sans-serif;
    font-optical-sizing: auto;
    font-weight: 300;
    font-style: normal;
}

.footercontent{
    display: flex;
    flex-direction: column;
    padding-left: 50px;
    list-style: none;

}

.footerbanner{
    background-color: #000;
    display: flex;
    flex-direction: column;
    align-items: center;
    font-size: 12px;
}

ul{
    padding: 20px 0px 20px 0px;
    list-style: none;

    li{
        font-size: 16px;
        padding: 5px;
    }
}

.some{
    margin: 20px 0px;
}

.some font-awesome-icon {
    font-size: 100px;
    margin: 0 10px;
}


.logo{
    margin: 20px 50px 20px 0px;
}

@media screen {
    
}
</style>