<script setup>
import {defineProps, defineEmits} from 'vue'
    let props = defineProps({
        id: {
            type: Number,
        },
        img: {
            type: String,
        },
        name:{
            type: String,
        },
        price:{
            type: Number,
        }
    })
</script>

<template>
    <div class="card">
        <div class="image">
            <img :src="img">
        </div>
        <span class="card__title">{{ name }}</span>
        <span class="card__price">{{ price }} руб.</span>
        <button class="button"
                @click="emits('addToCart', id)"
                >Купить</button>
    </div>
</template>

<style scoped>

.card{
    background-color: #FFFFFF;
    width: 250px;
    display: flex;
    flex-direction: column;
    gap: 15px;
    padding: 20px;
    border-radius: 15px;
    box-shadow: 8px 5px 10px rgba(11, 11, 11, 0.5);
}

img{
    max-width: 100%;
    height: 100%;
}

.image{
    height: 220px;
    margin: 0 auto;
    margin-bottom: auto;
}


.card__title{
    font-size: 30px;
    font-family: Impact, Haettenschweiler, 'Arial Narrow Bold', sans-serif;
    color: #34B0D6;
    width: bold;

}

.card__price{
    font-size: 25px;
    font-family: 'Gill Sans', 'Gill Sans MT', Calibri, 'Trebuchet MS', sans-serif;
}


</style>