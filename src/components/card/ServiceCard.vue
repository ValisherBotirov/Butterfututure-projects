<template>
  <div class="grid grid-cols-1 sm:grid-cols-2 dm:grid-cols-3 gap-7 mt-8">
    <div
      v-for="item in serviceData"
      :key="item?.id"
      class="card py-5 rounded-[19px] bg-[#74636314]"
    >
      <div class="flex flex-col items-center">
        <img
          class="max-w-[70px] my-3"
          src="../../assets/svg/logo-white.svg"
          alt="icon academy"
        />
        <p class="text-white leading-[43.57px] font-bold text-3xl dm:text-4xl">
          {{ item.job }}
        </p>
        <p class="text-white px-5 text-[15px] pt-10">{{ item?.text }}</p>
      </div>
      <button
        class="w-[90%] bg-[#FFD100] mx-auto block rounded-md py-2 font-bold mt-5 text-[#333]"
      >
        Aloqaga chiqish
      </button>
    </div>
  </div>
</template>
<script setup>
const serviceData = [
  {
    job: "Veb sayt",
    icon: "fa-brands fa-apple",
    text: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Provident, laudantium. Lorem ipsum dolor sit amet consectetur adipisicing elit. Provident, laudantium.",
    id: 1,
  },
  {
    job: "Veb ilova",
    icon: "fa-brands fa-apple",
    text: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Provident, laudantium. Lorem ipsum dolor sit amet consectetur adipisicing elit. Provident, laudantium.",
    id: 1,
  },
  {
    job: "Android ilova",
    icon: "fa-brands fa-apple",
    text: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Provident, laudantium. Lorem ipsum dolor sit amet consectetur adipisicing elit. Provident, laudantium.",
    id: 2,
  },
  {
    job: "iOS ilova",
    icon: "fa-brands fa-apple",
    text: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Provident, laudantium. Lorem ipsum dolor sit amet consectetur adipisicing elit. Provident, laudantium.",
    id: 4,
  },
  {
    job: "Telegram bot",
    icon: "fa-brands fa-apple",
    text: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Provident, laudantium. Lorem ipsum dolor sit amet consectetur adipisicing elit. Provident, laudantium.",
    id: 1,
  },
  {
    job: "CRM tizimi",
    icon: "fa-brands fa-apple",
    text: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Provident, laudantium. Lorem ipsum dolor sit amet consectetur adipisicing elit. Provident, laudantium.",
    id: 1,
  },
];
</script>
<style scoped>
.card {
  transition: all 0.2s linear;
  transform: scale(0.96);
}
.card:hover {
  cursor: pointer;
  transform: scale(0.97);
  transition: all 0.2s linear;
  box-shadow: 0px 0px 15px 5px #fafcf5;
}
</style>
