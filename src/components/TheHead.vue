<script setup>
    import { Swiper, SwiperSlide } from 'swiper/vue';
    import 'swiper/css';
    import 'swiper/css/navigation';
    import 'swiper/css/pagination';
    import { Navigation, Pagination } from 'swiper/modules';
    const modules = [Navigation, Pagination];

    import TheCard from './TheCard.vue';
    import TheCatalog from './TheCatalog.vue';
    import {ref, computed, defineProps} from 'vue';
    
    const props = defineProps({
        toys: {
            type: Array,
        }
    });
    
    console.log('Дочерний получил:', props.toys)
</script>

<template>
    <h1>Популярные товары</h1>
    <swiper
    
    :modules="modules" 
    :slides-per-view="1" 
    :navigation="true" 
    :pagination="true">
        <swiper-slide>
            <the-card/>
        </swiper-slide>
        <swiper-slide>
            <the-card/>
        </swiper-slide>
        <swiper-slide>
            <the-card/>
        </swiper-slide>
    </swiper>
</template>

<style scoped>

</style>