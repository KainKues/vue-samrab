<script setup>
    import TheReview from './TheReview.vue';
    import { ref } from 'vue';
    const reviews = ref([]); 
    const review = ref({
        id: 0,
        name: '',
        email: '',
        content: '',
    });

    function submit() {
        reviews.value.push(review.value)
        review.value = {
        id: '',
        name: '',
        email: '',
        content: '',
    };  
      console.log(reviews.value);
  }

</script>

<template>
    <form class="window">
        <input 
            class="window__name" 
            type="" 
            placeholder="Имя" 
            required
            v-model="review.name"
            >
        <input 
            class="window__email" 
            type="email" 
            placeholder="Почта" 
            required
            v-model="review.email"
            >
        <textarea 
            class="window__review" 
            placeholder="Оставьте свой отзыв" 
            required
            v-model="review.content"
            ></textarea>
        <button class="button"
                @click.prevent="submit"
        >Отправить</button>
    </form>
    <div class="contain"
        v-if="reviews.length"
        >
        <TheReview
            v-for="item in reviews"
            :key="item.id"    
            :name="item.name"
            :email="item.email"
            :content="item.content"
        />
    </div>
</template>
  
<style scooped>
    .window{
        background-color: white;
        width: 40%;
        margin: 0 auto 50px;
        border-radius: 20px;
        box-shadow: 8px 5px 10px rgba(11, 11, 11, 0.5);

        display: flex;
        flex-direction: column;
        padding: 40px;
        gap: 30px;
    }


    .window input, textarea{
        height: 40px;
        border-radius: 10px;
        border: none;
        background-color: rgb(221, 213, 213);
        padding: 0 10px;
        font-family: 'Gill Sans', 'Gill Sans MT', Calibri, 'Trebuchet MS', sans-serif;
        font-size: 18px;
    }

    .window__review{
        height: 120px;
        padding-top: 10px;
    }

    .contain{
        background-color: white;
        border-radius: 10px;
        padding: 40px;
        display: flex;
        flex-direction: column;
        gap: 20px;
    }
</style>