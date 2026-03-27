<script setup>
import { RouterLink, RouterView } from 'vue-router'

</script>

<template>
    <div class="sidebar">
        <nav class="sidebar__nav">
            <RouterLink to="/">ГЛАВНАЯ</RouterLink>
            <RouterLink to="/about">О НАС</RouterLink>
            <RouterLink to="/catalog">КАТАЛОГ</RouterLink>
        </nav>
    </div>
    <div class="page">
            <RouterView></RouterView>
    </div>
</template>

<style scoped>

    
    .sidebar{
        position: fixed;
        left: 0;
        top:0;
        bottom: 0;
        background-color: rgb(255, 251, 251);
        max-width: max-content;
        padding-right: 30px;
    }

    .sidebar__nav{
        display: flex;
        flex-direction: column;
        padding: 30px;
        font-size: 26px;
        font-family: 'Gill Sans', 'Gill Sans MT', Calibri, 'Trebuchet MS', sans-serif;
    }

</style>
