<template>
    <div class="w-full">
      <Swiper 
        :modules="modules"
        class="swiper-container "
        :slides-per-view="1.9"
        :loop="true"
        :space-between="20"
      >
        <SwiperSlide 
          v-for="(item, index) in swiperItems"
          :key="index"
          class="slide-item"
        >
          <img :src="item.img" class="w-full h-auto rounded-lg">
          <div class="flex flex-col mt-5">
            <p class="text-lg text-gray-500">{{ item.time }}</p>
            <p class="mt-2 text-2xl font-semibold text-gray-900">{{ item.title }}</p>
            <p class="mt-4 text-lg text-gray-600">{{ item.des }}</p>
          </div>
        </SwiperSlide>
      </Swiper>
    </div>
  </template>

<script setup>
import {Swiper, SwiperSlide} from 'swiper/vue';
import 'swiper/css';
import 'swiper/css/pagination';
import 'swiper/css/navigation';
import { Navigation, Pagination } from 'swiper/modules';

const modules = [Navigation, Pagination];

const swiperItems=[
    {
        img: '/img/dogInSwiper1.svg',
        time:'12 March, 2023',
        title: 'Keep Your Pets Cozy This Winter! 🐾 ',
        des: "We've just stocked up on stylish and warm winter coats for your furry friends! From small pups to big dogs, we have sizes to keep every pet comfortable during chilly walks. Visit us in-store or online to check out our collection. Don’t let the cold stop your adventures!"
    },
    {
        img: '/img/dogInSwiper2.svg',
        time:'12 March, 2023',
        title: 'Fresh Breath, Happy Pets! 🦷 ',
        des: "Did you know that regular dental care can add years to your pet’s life? Check out our range of dental chews, toothbrushes, and pet-safe toothpaste to keep their teeth sparkling clean and healthy. Stop by today for expert advice on maintaining your pet’s oral hygiene."
    },
    {
        img: '/img/dogInSwiper1.svg',
        time:'12 March, 2023',
        title: 'Keep Your Pets Cozy This Winter! 🐾 ',
        des: "We've just stocked up on stylish and warm winter coats for your furry friends! From small pups to big dogs, we have sizes to keep every pet comfortable during chilly walks. Visit us in-store or online to check out our collection. Don’t let the cold stop your adventures!"
    },
    {
        img: '/img/dogInSwiper2.svg',
        time:'12 March, 2023',
        title: 'Fresh Breath, Happy Pets! 🦷 ',
        des: "Did you know that regular dental care can add years to your pet’s life? Check out our range of dental chews, toothbrushes, and pet-safe toothpaste to keep their teeth sparkling clean and healthy. Stop by today for expert advice on maintaining your pet’s oral hygiene."
    },
    {
        img: '/img/dogInSwiper1.svg',
        time:'12 March, 2023',
        title: 'Keep Your Pets Cozy This Winter! 🐾 ',
        des: "We've just stocked up on stylish and warm winter coats for your furry friends! From small pups to big dogs, we have sizes to keep every pet comfortable during chilly walks. Visit us in-store or online to check out our collection. Don’t let the cold stop your adventures!"
    },
    {
        img: '/img/dogInSwiper2.svg',
        time:'12 March, 2023',
        title: 'Fresh Breath, Happy Pets! 🦷 ',
        des: "Did you know that regular dental care can add years to your pet’s life? Check out our range of dental chews, toothbrushes, and pet-safe toothpaste to keep their teeth sparkling clean and healthy. Stop by today for expert advice on maintaining your pet’s oral hygiene."
    },
    {
        img: '/img/dogInSwiper1.svg',
        time:'12 March, 2023',
        title: 'Keep Your Pets Cozy This Winter! 🐾 ',
        des: "We've just stocked up on stylish and warm winter coats for your furry friends! From small pups to big dogs, we have sizes to keep every pet comfortable during chilly walks. Visit us in-store or online to check out our collection. Don’t let the cold stop your adventures!"
    },
    {
        img: '/img/dogInSwiper2.svg',
        time:'12 March, 2023',
        title: 'Fresh Breath, Happy Pets! 🦷 ',
        des: "Did you know that regular dental care can add years to your pet’s life? Check out our range of dental chews, toothbrushes, and pet-safe toothpaste to keep their teeth sparkling clean and healthy. Stop by today for expert advice on maintaining your pet’s oral hygiene."
    },
]

</script>

<style scoped>
:deep(.swiper) {
  width: 100%;
  overflow: hidden;
}

/* Kiểm soát kích thước và bố cục slide */
:deep(.swiper-slide) {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  background-color: white;
  border-radius: 12px;
  padding: 20px;
  box-shadow: 0 4px 10px rgba(0, 0, 0, 0.1);
}
</style>