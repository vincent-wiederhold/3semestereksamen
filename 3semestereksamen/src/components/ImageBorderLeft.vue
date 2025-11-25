<script setup>
defineProps({
    src: String,
    alt: String
});
</script>

<template>
<div class="imageborder">
    <img :src="src" :alt="alt">
</div>
</template>

<style scoped>
    .imageborder {
        position: relative;
        display: inline-block;

        img {
            z-index: 2;
            display: block;
            height: 100%;
            width: 600px;
            position: relative;
        }
    }

    .imageborder::after {
        position: absolute;
        content: '';
        top: 5%;
        right: 5%;
        border: 8px solid #AF3238;
        height: 100%;
        width: 100%;
    }
</style>