<script setup>
    import { defineProps } from 'vue';
    let props = defineProps({
        id: {
            type: Number,
        },
        name:{
            type: String,
        },
        email:{
            type: String,
        },
        content:{
            type: String,
        }
    })
</script>

<template>
    <div class="review">
        <span class="review__name">{{ name }}</span>
        <span class="review__content">{{ content}}</span>
    </div>
</template>

<style>
    .review{
        background-color: #d8d2d2;
        display: flex;
        flex-direction: column;
        gap: 15px;
        padding: 20px;
        border-radius: 15px;
        box-shadow: 8px 5px 10px rgba(11, 11, 11, 0.5);
        font-size: 18px;
        color: rgb(63, 58, 58);
        font-family: 'Gill Sans', 'Gill Sans MT', Calibri, 'Trebuchet MS', sans-serif;
    }
</style>