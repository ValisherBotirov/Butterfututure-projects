<template>
  <section class="bg-[#0F0A2B] py-6 pb-8 mt-8">
    <div class="flex gap-4 items-center justify-center">
      <p class="text-white inline flex-shrink-0 leading-[19.36px]">
        <span class="text-[#7F43FF] font-[400]"
          >03 <span class="px-1 pr-2 font-bold">|</span> </span
        >Bizning jamoa
      </p>
    </div>
    <h2
      class="font-['HuboSans'] leading-[34.81px] text-white font-semibold text-[28px] sm:text-[32px] text-center mt-4 sm:mt-4 max-w-[571px] mx-auto mb-6"
    >
      Bizning jamoa
    </h2>

    <div
      class="container grid grid-cols-1 ms:grid-cols-2 md:!grid-cols-3 dm:!grid-cols-4 gap-3 ms:gap-6"
    >
      <TeamCard v-for="item in teamCard" :key="item" :data="item" />
    </div>
  </section>
</template>

<script setup lang="ts">
import TeamCard from "@/components/card/TeamCard.vue";
function getImageUrl(name: string) {
  return new URL(`../assets/team/${name}`, import.meta.url).href;
}

const teamCard = [
  {
    id: 1,
    name: "Valisher Botirov",
    position: "Frontend Developer",
    image: getImageUrl("valisher.jpg"),
    socials: [],
  },
  {
    id: 2,
    name: "Shohruh Soatov",
    position: "CEO",
    socials: [],
    image: getImageUrl("shohruh_aka.jpg"),
  },
  {
    id: 3,
    name: "Nodir Ikromov",
    position: "Frontend Developer",
    socials: [],
    image: getImageUrl("nodir.jpg"),
  },
  {
    id: 4,
    name: "Javohir Orifjonov",
    position: "Backend Developer",
    socials: [],
    image: getImageUrl("shohruh_aka.jpg"),
  },
  // {
  //     id:5,
  //     name:'Elbek Xolmatov',
  //     position: "Backend Developer",
  //     socials: [],
  //     image:'https://media.licdn.com/dms/image/D4D03AQGOq3IJmSa5Wg/profile-displayphoto-shrink_800_800/0/1669657302377?e=2147483647&v=beta&t=4mCJH01uxnDK0hsulCtOE8bYbodVckDc9RItNPM1-zE'
  // }
];
</script>
