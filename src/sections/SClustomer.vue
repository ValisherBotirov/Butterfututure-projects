<template>
  <div class="container pt-16 md:pt-[82px]">
    <h2
      class="text-[#1F2937] font-semibold text-xl md:text-[40px] leading-8 md:leading-[48px] text-center"
    >
      Наши довольные вендоры
    </h2>
    <swiper
      :slidesPerView="3"
      :spaceBetween="32"
      :modules="[Autoplay]"
      :loop="true"
      :autoplay="true"
      :delay="300"
      :breakpoints="{
        '320': { slidesPerView: 1.2, spaceBetween: 15 },
        '480': { slidesPerView: 1, spaceBetween: 20 },
        '768': { slidesPerView: 3, spaceBetween: 32 },
      }"
      class="mySwiper mt-8 md:mt-12"
    >
      <swiper-slide v-for="(item, index) in customerData" :key="index">
        <CustomerCard :data="item" class="ms:mx-[20px] md:!mx-[0px]" />
      </swiper-slide>
    </swiper>
  </div>
</template>

<script setup lang="ts">
import CustomerCard from "@/components/card/CustomerCard.vue";
import { Swiper, SwiperSlide } from "swiper/vue";
import "swiper/css";
import { Autoplay } from "swiper/modules";
const customerData = [
  {
    id: 1,
    images: "user1",
    text: "When our designs need an expert opinion or approval, I know I can rely on your agency Thank you for all your help-I will be recommending you to everyone",
  },
  {
    id: 2,
    images: "user2",
    text: "When our designs need an expert opinion or approval, I know I can rely on your agency Thank you for all your help-I will be recommending you to everyone",
  },
  {
    id: 3,
    images: "user3",
    text: "When our designs need an expert opinion or approval, I know I can rely on your agency Thank you for all your help-I will be recommending you to everyone",
  },
];
</script>
