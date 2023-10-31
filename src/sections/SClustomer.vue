<template>
  <div class="container pt-[80px] sm:pt-[90px]">

    <div
      class="grid grid-cols-1 md:grid-cols-3 gap-[90px] md:!gap-[21px] mt-[140px] ms:mt-[160px]"
    >
      <CustomerCard
        v-for="(item, index) in customerData"
        :key="index"
        :data="item"
        class="ms:mx-[20px] md:!mx-[0px]"
      />
    </div>
  </div>
</template>

<script setup lang="ts">
import CustomerCard from "@/components/card/CustomerCard.vue";
const customerData = [
  {
    id: 1,
    images: "customer.png",
    idea: "Top Jamoa! Natija super.",
    name: "Javohir K.",
    position: "Direktor",
  },
  {
    id: 2,
    images: "customer2.png",
    idea: "Shubhasiz barchaga tavsiya qilaman!",
    name: "Mavluda A.",
    position: "Bosh Menedjer",
  },
  {
    id: 3,
    images: "customer3.png",
    idea: "Rahmat! Jamoa ishlari juda yoqdi.",
    name: "Karimjon N.",
    position: "Menedjer",
  },
];
</script>

<style scoped>
.linear {
  background: linear-gradient(
    90deg,
    rgba(255, 255, 255, 0.5) -1.52%,
    rgba(0, 0, 0, 0) 109.98%
  );
}
.gradient {
  box-shadow: 0px 0px 30px 0px #fdf001, inset 0px 0px 4px 0px #ffffff;
  background: #fdf001;
}
</style>
