<template>
  <div class="relative">

  <div class="container pt-5 md:pt-[72px]">
    <div class="flex flex-col-reverse md:grid md:grid-cols-2 gap-5 md:gap-8">
      <div class="md:py-[50px]">
        <div>
          <h2
            class="text-[#1F2937] font-semibold text-2xl md:text-[40px] leading-8 md:leading-[48px] max-w-[600px]"
          >
            Раскрой свой потенциал вместе с Coozin!
          </h2>
          <p class="mt-3 md:mt-4 text-[#4B5563] font-normal leading-6">
            Универсальная платформа Coozin предоставляют множество возможностей
            для самозанятых женщин. На платформе можно продавать товары и
            услуги, а также учиться новым навыкам и развивать свой бизнес
          </p>
          <SButton
            custom-class="md:!max-w-[200px]"
            class="mt-6 dm:mt-7"
            @click="openModal = true"
          >
            {{ $t("connect") }}
          </SButton>
        </div>
        <div class="hidden md:block md:mt-[150px]">
          <p class="text-[#374151]">Достижения</p>
          <div class="grid grid-cols-3 gap-4 mt-4 text-xl">
            <div>Item 1</div>
            <div>Item 2</div>
            <div>Item 3</div>
          </div>
        </div>
      </div>
      <div class="grid grid-cols-3 gap-3 md:gap-5">
        <div class="col-span-2 max-h-[316px]">
          <img
            src="@/assets/images/banner4.png"
            alt="images"
            class="w-full h-full object-cover rounded-[16px]"
          />
        </div>
        <div class="max-h-[316px]">
          <img
            src="@/assets/images/banner2.png"
            alt="images"
            class="w-full h-full object-cover rounded-[16px]"
          />
        </div>
        <div class="max-h-[316px]">
          <img
            src="@/assets/images/banner3.png"
            alt="images"
            class="w-full h-full object-cover rounded-[16px]"
          />
        </div>
        <div class="col-span-2 max-h-[316px]">
          <img
            src="@/assets/images/banner1.png"
            alt="images"
            class="w-full h-full object-cover rounded-[16px]"
          />
        </div>
      </div>
    </div>
    <div class="grid grid-cols-1 md:grid-cols-2 gap-6 md:gap-[140px] mt-6 md:mt-12 items-center">
      <div class="">
        <img
          src="@/assets/images/banner-bottom.png"
          alt="banner images"
          class="w-full h-[284px] md:h-full object-cover rounded-[16px]"
        />
      </div>
      <div>
        <h2
          class="text-[#1F2937] font-semibold text-2xl md:text-[40px] leading-8 md:leading-[48px] max-w-[600px]"
        >
          EDU COOZIN
        </h2>
        <p class="mt-3 md:mt-4 text-[#4B5563] font-normal leading-6">
          Онлайн-академия Coozin предоставляет обучение и помощь в развитии
          бизнеса.
        </p>
        <div class="mt-[26px] md:mt-[56px] flex flex-col gap-6 md:gap-[34px]">
          <BannerCard v-for="item in bannerList" :key="item.id" v-bind="item" />
        </div>
      </div>
    </div>
    <SModal :is-open="openModal" @closeModal="(e) => (openModal = e)" />
  </div>
    <img src="@/assets/images/banner-right.svg" alt="banner images" class="absolute right-0 top-[-90px] -z-1 hidden lg:block">
  </div>
</template>
<script setup lang="ts">
import { ref } from "vue";
import SButton from "@/components/SButton.vue";
import SModal from "@/components/modal/SModal.vue";
import BannerCard from "@/components/card/BannerCard.vue";
const openModal = ref(false);

const bannerList = [
  {
    id: 1,
    title: "Курсы и мастер-классы",
    description:
      "На платформе доступны онлайн-курсы и мастер-классы по различным темам, связанным с бизнесом, такими как управление продажами, маркетинг, финансы и другие.",
  },
  {
    id: 2,
    title: "Опытные специалисты",
    description:
      "Курсы ведут опытные специалисты, которые делятся своими знаниями и опытом.\n",
  },
  {
    id: 3,
    title: "Обучись и начни свое дело",
    description:
      "Пользователи которые успешно прошли курсы имеют возможность\n" +
      "присоединиться к торговой площадке Coozin.",
  },
];
</script>
