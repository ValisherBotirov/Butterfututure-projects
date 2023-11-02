<template>
  <div class="container pt-12 md:pt-[120px]">
    <div class="flex items-center justify-between">
      <div class="swiper-button-prev cursor-pointer text-2xl hidden md:block">&larr;</div>

      <h2
        class="text-[#1F2937] font-semibold text-2xl md:text-[40px] leading-8 md:leading-[48px] text-center"
      >
        Мероприятия
      </h2>
      <div class="swiper-button-next cursor-pointer text-2xl md:block">&rarr;</div>
    </div>
    <div class="mt-5 md:mt-12">
      <swiper
        :slidesPerView="3"
        :spaceBetween="32"
        :modules="[Autoplay, Navigation]"
        :loop="true"
        :autoplay="true"
        :delay="300"
        :pauseOnMouseEnter="true"
        :breakpoints="{
          '320': { slidesPerView: 1.5, spaceBetween: 15 },
          '480': { slidesPerView: 2, spaceBetween: 20 },
          '768': { slidesPerView: 3, spaceBetween: 32 },
        }"
        class="mySwiper"
      >
        <swiper-slide v-for="(item, index) in sliderData" :key="index">
          <MetropCard class="cursor-pointer" v-bind="item" />
        </swiper-slide>
      </swiper>
    </div>
  </div>
</template>

<script setup lang="ts">
import { Autoplay, Navigation } from "swiper/modules";
import { Swiper, SwiperSlide } from "swiper/vue";
import MetropCard from "@/components/card/MetropCard.vue";
import "swiper/css";


const sliderData = [
  {
    id: 1,
    image: "slider1",
  },
  {
    id: 2,
    image: "slider2",
  },
  {
    id: 3,
    image: "banner1",
  },
  {
    id: 4,
    image: "banner4",
  }
];
</script>
