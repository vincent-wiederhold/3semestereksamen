<script setup>
import { ref } from 'vue';

const toggle = ref(false);

const dropdownToggle = () => {
    toggle.value = !toggle.value;
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

        <div id="katalog-dropdown" v-if="toggle">
            <ul class="dropdown-kategori">
                <li class="kategori-navn">Keramik og glas</li>
                <li class="kategori-link"><a href="">Krus og kopper</a></li><hr class="divider-line">
                <li class="kategori-link">Skåle</li><hr class="divider-line">
                <li class="kategori-link">Kander</li><hr class="divider-line">
                <li class="kategori-link">Fade og tallerkener</li><hr class="divider-line">
                <li class="kategori-link">Vaser</li><hr class="divider-line">
                <li class="kategori-link">Lys og lamper</li><hr class="divider-line">
                <li class="kategori-link">Urtekopper</li><hr class="divider-line">
                <li class="kategori-link">Andre keramiske sager</li><hr class="divider-line">
            </ul>
            <ul class="dropdown-kategori">
                <li class="kategori-navn">Smykker</li><hr class="divider-line">
                <li class="kategori-link">Halskæder</li><hr class="divider-line">
                <li class="kategori-link">Øreringe</li><hr class="divider-line">
                <li class="kategori-link">Ringe</li><hr class="divider-line">
                <li class="kategori-link">Armbånd</li><hr class="divider-line">
                <li class="kategori-link">Brocher</li><hr class="divider-line">
            </ul>
            <ul class="dropdown-kategori">
                <li class="kategori-navn">Unika</li><hr class="divider-line">
                <li class="kategori-link">Vaser</li><hr class="divider-line">
                <li class="kategori-link">Skåle</li><hr class="divider-line">
                <li class="kategori-link">Badekar</li><hr class="divider-line">
                <li class="kategori-link">Objekter</li><hr class="divider-line">
                <li class="kategori-link">Fade</li><hr class="divider-line">
            </ul>
            <ul class="dropdown-kategori">
                <li class="kategori-navn">Til væggen</li><hr class="divider-line">
                <li class="kategori-link">Vægobjekter</li><hr class="divider-line">
                <li class="kategori-link">Grafik</li><hr class="divider-line">
                <li class="kategori-link">Originale tegninger</li><hr class="divider-line">
            </ul>
            <ul class="dropdown-kategori">
                <li class="kategori-navn">Diverse</li><hr class="divider-line">
                <li class="kategori-link">Snedkeri</li><hr class="divider-line">
                <li class="kategori-link">Hornvarer</li><hr class="divider-line">
                <li class="kategori-link">Tasker og punge</li><hr class="divider-line">
                <li class="kategori-link">Puder og tekstiler</li><hr class="divider-line">
                <li class="kategori-link">Jul og julepynt</li><hr class="divider-line">
                <li class="kategori-link">Flag og ranker</li><hr class="divider-line">
                <li class="kategori-link">Kort og gavekort</li><hr class="divider-line">
            </ul>
        </div>
    </nav>
    
</template>

<style>
</style>