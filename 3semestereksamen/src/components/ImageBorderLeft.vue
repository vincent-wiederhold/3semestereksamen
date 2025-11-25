<script setup>
defineProps({
    src: String,
    alt: String
});
</script>

<template>
<div class="imageborder">
    <img :src="src" :alt="alt">
    <div class="border"></div>
</div>
</template>

<style scoped>
    .border {
        position: relative;
        top: 10px;
        left: 10px;
        border: 8px solid;
        border-color: blueviolet;
        height: 500px;
        width: 500px;
        z-index: 1;
    }

    .imageborder {
        margin: 100px;
        img {
            z-index: 2;
            display: block;
            height: 100%;
            width: 700px;
            position: relative;
            

        }
    }

</style>