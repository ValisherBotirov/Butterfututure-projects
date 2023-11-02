<template>
  <div class="container text-center w-full pt-10 md:pt-[80px]">
    <div class="hidden md:block">
      <div class="flex justify-center">
        <img src="@/assets/icon/footer/logo.svg" alt="logo svg" />
      </div>
      <div class="flex gap-8 items-center text-[1F2937] justify-center mt-10">
        <p class="cursor-pointer hover:text-[#FF6600]">О нас</p>
        <p class="cursor-pointer hover:text-[#FF6600]">Edu Coozin</p>
        <p class="cursor-pointer hover:text-[#FF6600]">Почему Coozin?</p>
        <p class="cursor-pointer hover:text-[#FF6600]">Присоединиться</p>
        <p class="cursor-pointer hover:text-[#FF6600]">Мероприятия</p>
      </div>
      <div class="flex items-center gap-7 mt-10 justify-center">
        <p class="text-[#374151]">При поддержке</p>
        <img src="@/assets/icon/footer/cola.png" alt="logo" />
        <img src="@/assets/icon/footer/osce.png" alt="logo" />
      </div>
      <div class="mt-[56px] flex items-center justify-center gap-6">
        <p class="text-[#1F2937] flex items-center gap-4">
          ПОДПИСЫВАЙТЕСЬ НА НАС <span class="w-16 h-[2px] bg-[#1F2937]"></span>
        </p>
        <SocialBox
          v-for="(item, i) in socialLinks"
          :key="i"
          :icon="item.icon"
          :link="item.link"
        />
      </div>
    </div>
    <div class="md:hidden flex justify-between items-end">
      <div class="flex gap-2">
        <SocialBox
          class="!w-8 !h-8"
          v-for="(item, i) in socialLinks"
          :key="i"
          :icon="item.icon"
          :link="item.link"
        />
      </div>
      <div class="flex justify-center">
        <img
          src="@/assets/icon/footer/logo.svg"
          class="w-[61px]"
          alt="logo svg"
        />
      </div>
    </div>
    <p class="text-[#1F2937] font-[400] text-sm mt-7 md:mt-10 pb-4 md:pb-10">
      © 2023 Coozin. All Rights Reserved
    </p>
  </div>
</template>
<script setup lang="ts">
import SocialBox from "@/components/SocialBox.vue";

const socialLinks = [
  {
    link: "https://www.instagram.com/valisher-botirov/",
    icon: "instagram",
  },
  {
    link: "https://www.instagram.com/valisher-botirov/",
    icon: "facebook",
  },
  {
    link: "https://www.instagram.com/valisher-botirov/",
    icon: "youtube",
  },
];
</script>
