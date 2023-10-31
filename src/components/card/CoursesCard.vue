<template>
  <div class="course min-h-[470px] h-full relative">
    <div
      class="card-side front group border border-transparent text-center bg-[#0F0A2B] hover:bg-transparent hover:border-[#6c63ff]"
      :class="isClick ? 'rotate-front-1' : ''"
    >
      <div>
        <img
          :src="data?.image"
          alt="images"
          class="h-[230px] w-full object-cover"
        />
      </div>
      <div class="py-4 pb-4 text-white">
        <h4 class="font-medium text-2xl">{{ data?.title }}</h4>
        <p class="mt-2">
          {{ data?.description }}
        </p>

        <div
          class="btn btn-primary py-3 px-5 transition duration-300 border border-[#F75842] inline-block cursor-pointer bg-[#F75842] group-hover:border-white group-hover:bg-transparent mt-4"
          @click="readMore"
        >
          Batafsil
        </div>
      </div>
    </div>
    <div
      class="card-side back text-white group border border-transparent bg-[#0F0A2B] hover:bg-transparent hover:border-[#6c63ff] py-4 px-3 flex flex-col justify-between text-center"
      :class="isClick ? 'rotate-back-1' : ''"
    >
      <div class="w-full mx-auto">
        <div class="flex justify-center flex-col">
          <i class="fa-solid fa-square-check text-green-500 text-4xl"></i>
          <p class="text-lg mt-2">{{ data?.moreContent?.title }}</p>
        </div>
        <ul class="mt-6 w-full mx-auto">
          <li
            v-for="item in data?.moreContent?.technology"
            :key="item"
            class="mt-1 list-disc flex items-center justify-center gap-3"
          >
            <span class="w-1.5 h-1.5 rounded-[50%] bg-white"></span>
            {{ item }}
          </li>
        </ul>
      </div>
      <div
        class="btn btn-primary py-3 px-4 transition duration-300 border border-[#F75842] inline-block cursor-pointer bg-[#F75842] group-hover:border-white group-hover:bg-transparent mt-4 text-center"
        @click="readMore"
      >
        Orqaga qaytish
      </div>
    </div>
  </div>
</template>

<script setup lang="ts">
import { ref } from "vue";

interface Props {
  data?: {
    title: string;
    image: string;
    description: string;
    moreContent?: {
      title: string;
      technology: string[];
    };
  };
}

defineProps<Props>();

const isClick = ref(false);
function readMore() {
  isClick.value = !isClick.value;
}
</script>

<style scoped>
.course {
  transition: all 0.4s;
  perspective: 150rem;
}

.back {
  transform: rotateY(-180deg);
}

.card-side {
  transition: all 0.8s ease;
  backface-visibility: hidden;
  position: absolute;
  top: 0;
  left: 0;
  height: 100%;
}

.rotate-front-1 {
  transform: rotateY(180deg);
}
.rotate-front-2 {
  transform: rotateY(0deg);
}
.rotate-back-1 {
  transform: rotateY(0deg);
}
.rotate-back-2 {
  transform: rotateY(-1800deg);
}
</style>
