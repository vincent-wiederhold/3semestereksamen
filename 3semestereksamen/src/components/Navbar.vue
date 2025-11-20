<script setup>
import { ref } from 'vue';

const isOpen = ref(false);

const dropdownToggle = () => {
    isOpen.value = !isOpen.value;
};

</script>

<template>
    <nav>
        <div id="menu-logo">
            <img src="../assets/dinavejling.svg" alt="Dina Vejling logo">
        </div>

        <div id="menu-items-desktop">
            <ul id="menu-punkter">
                <li>
                    <button @click="dropdownToggle" id="katalog-knap">
                        Katalog<font-awesome-icon icon="fa-solid fa-angle-down" />
                    </button>
                </li>
                <li><a href="">Arrangementer</a></li>
                <li><a href="">Kunstnere</a></li>
                <li><a href="">Galleri RUMMET</a></li>
                <li><a href="">Om os</a></li>
            </ul>
            <ul id="menu-icons">
                <li><font-awesome-icon icon="fa-solid fa-magnifying-glass" /></li>
                <li><font-awesome-icon icon="fa-solid fa-cart-shopping" /></li>
            </ul>
        </div>

        <div id="menu-items-mobile">
            <ul id="menu-icons">
                <li><font-awesome-icon icon="fa-solid fa-magnifying-glass" /></li>
                <li><font-awesome-icon icon="fa-solid fa-cart-shopping" /></li>
                <li>
                    <button @click="dropdownToggle" id="burgermenu">
                        <font-awesome-icon icon="fa-solid fa-bars" />
                    </button>
                </li>
            </ul>
        </div>

        <div id="katalog-dropdown" v-if="isOpen">
            <ul class="dropdown-kategori">
                <li class="kategori-navn">Keramik og glas</li>
                <li class="kategori-link">Krus og kopper</li>
                <li class="kategori-link">Skåle</li>
                <li class="kategori-link">Kander</li>
                <li class="kategori-link">Fade og tallerkener</li>
                <li class="kategori-link">Vaser</li>
                <li class="kategori-link">Lys og lamper</li>
                <li class="kategori-link">Urtekopper</li>
                <li class="kategori-link">Andre keramiske sager</li>
            </ul>
            <ul class="dropdown-kategori">
                <li class="kategori-navn">Smykker</li>
                <li class="kategori-link">Halskæder</li>
                <li class="kategori-link">Øreringe</li>
                <li class="kategori-link">Ringe</li>
                <li class="kategori-link">Armbånd</li>
                <li class="kategori-link">Brocher</li>
            </ul>
            <ul class="dropdown-kategori">
                <li class="kategori-navn">Unika</li>
                <li class="kategori-link">Vaser</li>
                <li class="kategori-link">Skåle</li>
                <li class="kategori-link">Badekar</li>
                <li class="kategori-link">Objekter</li>
                <li class="kategori-link">Fade</li>
            </ul>
            <ul class="dropdown-kategori">
                <li class="kategori-navn">Til væggen</li>
                <li class="kategori-link">Vægobjekter</li>
                <li class="kategori-link">Grafik</li>
                <li class="kategori-link">Originale tegninger</li>
            </ul>
            <ul class="dropdown-kategori">
                <li class="kategori-navn">Diverse</li>
                <li class="kategori-link">Snedkeri</li>
                <li class="kategori-link">Hornvarer</li>
                <li class="kategori-link">Tasker og punge</li>
                <li class="kategori-link">Puder og tekstiler</li>
                <li class="kategori-link">Jul og julepynt</li>
                <li class="kategori-link">Flag og ranker</li>
                <li class="kategori-link">Kort og gavekort</li>
            </ul>
        </div>
    </nav>
    
</template>

<style>
</style>