<template>
  <div class="relative">
    <div class="container pt-8 md:pt-[104px]">
      <div>
        <h2
          class="text-[#1F2937] font-semibold text-2xl md:text-[40px] leading-8 md:leading-[48px] text-center"
        >
          Почему Coozin?
        </h2>
        <div class="grid grid-cols-1 md:grid-cols-3 gap-7 md:gap-8 mt-12">
          <WhyUSCard v-for="item in data" :key="item.id" v-bind="item" />
        </div>
      </div>
      <div class="mt-8 md:mt-16 grid grid-cols-5 items-center gap-10">
        <div class="col-span-5 md:col-span-3">
          <h2
            class="text-[#1F2937] font-semibold text-xl md:text-[40px] leading-8 md:leading-[48px] max-w-[660px]"
          >
            Готовы присоединиться и развиваться вместе с нами?
          </h2>
          <div>
            <p
              class="mt-[6px] md:mt-4 font-normal leading-6 text-[#374151] md:text-xl"
            >
              Заполните форму, и мы свяжемся с вами!
            </p>
            <div
              class="grid grid-cols-1 md:grid-cols-2 gap-4 md:gap-7 mt-3 md:mt-6"
            >
              <SInput
                v-model="form.name"
                class="mt-3"
                input-class="!bg-white !py-3 !border-[#D1D5DB]"
                inputStyle="!text-black !placeholder:text-black "
                placeholder=""
                label="Фамилия"
                labelStyle="text-[#374151] font-medium"
              />
              <SInput
                v-model="form.surname"
                class="mt-3"
                input-class="!bg-white !py-3 !border-[#D1D5DB]"
                inputStyle="!text-black !placeholder:text-black "
                placeholder=""
                label="Имя"
                labelStyle="text-[#374151] font-medium"
              />
              <SInput
                v-model="form.phoneNumber"
                type="phone"
                class="mt-3 sm:mt-4"
                input-class="!bg-white !py-3 !border-[#D1D5DB]"
                inputStyle="!text-black !placeholder:text-black "
                placeholder="00 000-00-00"
                label="Номер телефона"
                labelStyle="text-[#374151] font-medium"
              >
                <template #prefix>
                  <p class="mr-2 font-bold text-sm sm:text-base">+998</p>
                </template>
              </SInput>
              <SSelect
                v-model="form.select"
                class="mt-3 sm:mt-4"
                :data="selectData"
                placeholder=" "
                label="Направление"
              />
              <SSelect
                v-model="form.select"
                class="mt-3 sm:mt-4"
                :data="selectData"
                placeholder=" "
                label="Город"
              />
              <SSelect
                v-model="form.select"
                class="mt-3 sm:mt-4"
                :data="selectData"
                placeholder=" "
                label="Район"
              />
            </div>
            <SButton
              custom-class="md:!max-w-[350px] mx-auto"
              class="mt-7 md:mt-12"
            >
              {{ $t("connect") }}
            </SButton>
          </div>
        </div>
        <div class="hidden md:grid md:col-span-2">
          <img src="@/assets/images/contact.png" alt="contact images" />
        </div>
      </div>
    </div>
    <!--    <img src="@/assets/images/banner-right.svg" alt="banner images" class="top-[-1200px] left-0 hidden lg:block">-->
  </div>
</template>

<script setup lang="ts">
import WhyUSCard from "@/components/card/WhyUSCard.vue";
import { reactive } from "vue";
import SInput from "@/components/form/SInput.vue";
import SSelect from "@/components/form/SSelect.vue";
import SButton from "@/components/SButton.vue";

const form = reactive({
  name: "",
  surname: "",
  phoneNumber: "",
  select: "",
  message: "",
});

const selectData = [
  {
    value: "Ташкент",
    label: "Ташкент",
  },
  {
    value: "Андижон",
    label: "Андижон ",
  },
  {
    value: "Бухоро ",
    label: "Бухоро ",
  },
  {
    value: "Жиззах ",
    label: "Жиззах ",
  },
  {
    value: "Қашқадарё  ",
    label: "Қашқадарё  ",
  },
  {
    value: "Навоий",
    label: "Навоий",
  },
  {
    value: "Самарқанд ",
    label: "Самарқанд ",
  },
  {
    value: "Сурхондарё ",
    label: "Сурхондарё ",
  },
  {
    value: "Фарғона ",
    label: "Фарғона ",
  },
];

const data = [
  {
    id: 1,
    title: "Универсальная платформа",
    description:
      "Предназначенная для самозанятых женщин превратить свое хобби в прибыльный бизнес",
    imgName: "1",
  },
  {
    id: 2,
    title: "Обучение и бизнес",
    description:
      "Женщины экономят время и ресурсы, которые могут быть направлены на развитие своего бизнеса",
    imgName: "2",
  },
  {
    id: 3,
    title: "Дополнительный заработок",
    description:
      "Домохозяйки могут стать партнерами нашего проекта и получить инструменты для управления своим бизнесом.",
    imgName: "3",
  },
];
</script>
