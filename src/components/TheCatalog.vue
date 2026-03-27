<script setup>
import TheCard from './TheCard.vue';
import {ref} from 'vue'
import TheHead from './TheHead.vue';

let toys = ref([
    {
      id: 1,
      img: "https://img.detmir.st/vShTyuFW6uXlztTq4DDkZaK9yFoFkacvQlIJ2WLbOUM/rs:fit:700:700/g:sm/aHR0cHM6Ly9jYXRhbG9nLWNkbi5kZXRtaXIuc3QvbWVkaWEvQVRPek1SVmNlTTVTRDR2OFkyaUhBZTRPaER3d3Nzc1hXcHAwbVViTVE2az0uanBlZw.webp",
      price: 5999,
      title:  'Домик для кукол Sylvanian Families',
    },
    {
      id: 2,
      img: "https://img.detmir.st/AlzaPuGmOwz6sbXEvSY8EY3v66O-1I1HBBDs1_8HGpw/rs:fit:700:700/g:sm/aHR0cHM6Ly9jYXRhbG9nLWNkbi5kZXRtaXIuc3QvbWVkaWEvYWVRc191Yll6eGZIVktkb3JGTWVvZFNabG4zOWlxNzAxdWNCcFc1bENEYz0uanBlZw.webp",
      price: 1119,
      title:  'Игрушка BabyGo Ежик',
    },
    {
      id: 3,
      img: "https://img.detmir.st/dLrpiNlfFjsh0Ofx9pVTrvhQUlUgVyDjUUmxzpT3igA/rs:fit:700:700/g:sm/aHR0cHM6Ly9jYXRhbG9nLWNkbi5kZXRtaXIuc3QvbWVkaWEvM0kyWTBUd2p2djVRdlZrOEM0V3F5YzJwaDNXblQ0andoY3FOem9icXg2az0uanBlZw.webp",
      price: 2999,
      title:  'Кукла модельная Monster High Frankie Stein',
    },
    {
      id: 4,
      img: "https://img.detmir.st/cBOrmAkBJn0CIJ-RhEDRJJ0yCri-a5lCw3srQlt2JhI/rs:fit:700:700/g:sm/aHR0cHM6Ly9jYXRhbG9nLWNkbi5kZXRtaXIuc3QvbWVkaWEvRHd0R3diTTR5RXN3M0VmZ2d3dk5PNW9uM3paalFyM2g2X1ZBQVg0NG5Zaz0uanBlZw.webp",
      price: 3999,
      title:  'Мягкая игрушка Moose Пингвинчик',
    },
    {
      id: 5,
      img: "https://img.detmir.st/Pvu6WOQzjexV4IrrohhzdxwSZKrDbyhqwMQ4vDylcq0/rs:fit:700:700/g:sm/aHR0cHM6Ly9jYXRhbG9nLWNkbi5kZXRtaXIuc3QvbWVkaWEvSUNZcWJZbTVlWDliUEVtTDNnOFVKUXV4Mm1ObHljRlpIaU9NREZ2eGRvST0uanBlZw.webp",
      price: 120,
      title:  'Лопата ZEBRA желтый',
    },
    {
      id: 6,
      img: "https://img.detmir.st/GI2ik4MMeK6A6X7vdnSOWYd9JjK1G5qfSTUSpxhUf34/rs:fit:700:700/g:sm/aHR0cHM6Ly9jYXRhbG9nLWNkbi5kZXRtaXIuc3QvbWVkaWEvaXJ3dmcteHZUcV8xNDZIdlJxeXVHOU5PZHhYa0JIbWZMMWNSRzY0WXhyWT0uanBlZw.webp",
      price: 1499,
      title:  'Караоке Attivio Три Кота',
    },
    {
      id: 7,
      img: "https://img.detmir.st/BzaVwT0vTIImrq5UURBv_D4lp7V1NV63jr9ukI7fjHY/rs:fit:700:700/g:sm/aHR0cHM6Ly9jYXRhbG9nLWNkbi5kZXRtaXIuc3QvbWVkaWEvazFGaUtqUnVLblFrRVZrZlBRNDdTT1Q2SDZlc010ZEZ2WktwSTNHV2ZtWT0uanBlZw.webp",
      price: 1799,
      title:  'Мягкая игрушка Laffi Корги Сплюша',
    },
    {
      id: 8,
      img: "https://img.detmir.st/-HRUvN05hFKhmoNXpUb13pFRSIMr9U5dsNLOc4JgCpw/rs:fit:700:700/g:sm/aHR0cHM6Ly9jYXRhbG9nLWNkbi5kZXRtaXIuc3QvbWVkaWEva05nOVdCRDZZZEg5eTM2R2Ewc0JVOW1mYkl2RzZ1bHV0VTZTdDlIMnJzND0uanBlZw.webp",
      price: 1699,
      title:  'Мягкая игрушка Смолтойс Чебурашка',
    },
    {
      id: 9,
      img: "https://img.detmir.st/L2Evthpo-EOkqjrdXI1Mt73BbyNTfS4y-rhD0O8pCCM/rs:fit:700:700/g:sm/aHR0cHM6Ly9jYXRhbG9nLWNkbi5kZXRtaXIuc3QvbWVkaWEvRm9KWm16TW5JSUsxYkFWemY2d3R3UWVsdWdmNm9TNjRQTndCTlBfVlZKND0uanBlZw.webp",
      price: 3999,
      title:  'Набор железнодорожный Mobicaro',
    },
    {
      id: 10,
      img: "https://img.detmir.st/D6HixFqxUKA2GWrJDcnSm0UG4wL1RgDdXRj1WEo_zBA/rs:fit:700:700/g:sm/aHR0cHM6Ly9jYXRhbG9nLWNkbi5kZXRtaXIuc3QvbWVkaWEvY1NXRGZwTTdOeHN0TExHWU1Sd09NUnFuMGwwUjVmMHAtTDZtSnd1bEhkaz0uanBlZw.webp",
      price: 3659,
      title:  'Пушкар Полесье Мотоцикл',
    },
    {
      id: 11,
      img: "https://img.detmir.st/ioZc6CFcoGl17epDAC80aCPgAfjczwnyYnkfK-NIpFo/rs:fit:700:700/g:sm/aHR0cHM6Ly9jYXRhbG9nLWNkbi5kZXRtaXIuc3QvbWVkaWEvU0E1eHJnNFRITmhvWnVJbEM2SWRtRjdLZU9zakE2eXFUcUdvSHl3RGd4az0uanBlZw.webp",
      price: 2999,
      title:  'Космический корабль Global Bros',
    },
    {
      id: 12,
      img: "https://img.detmir.st/_IazYUTozMA-1e2SLoDJ_Cvm7q0UdAwQwsrDhYt0kfo/rs:fit:700:700/g:sm/aHR0cHM6Ly9jYXRhbG9nLWNkbi5kZXRtaXIuc3QvbWVkaWEvX3pKX0RMX3ZwbXU2TTU0WWVJZmhoZXgwNUhWd2RzSmpqZFlkbXVxdXF2UT0uanBlZw.webp",
      price: 4999,
      title:  'Кукла пупс CRY BABIES Кэти',
    },
])

  console.log('Родитель передает:', toys.value)
</script>
  
<template>
  <div class="wrapper">
    <TheCard
      v-for="el in toys"
      :key ='el.id'
      :id="el.id"
      :img = 'el.img'
      :name = 'el.title'
      :price = 'el.price'
    />
    <TheHead :toys="toys" />
  </div>

</template>

<style scoped>
  .wrapper{
    margin-top: 40px;
    width: 100%;
    display: flex;
    flex-wrap: wrap;
    gap: 20px;
  }
</style>