<template>
  <div class="relative rounded-[10px] bg-[#9d9d91] py-3 px-7">
    <div class="flex justify-center mt-[70px] ms:mt-[80px]">
      <div class="text-center max-w-[306px] mx-auto">
        <p class="font-bold leading-[29.05px] text-lg text-white">
          {{ data?.idea }}
        </p>
        <p
          class="mt-4 ms:mt-[20px] font-bold leading-[24.2px] text-base ms:text-lg dm:text-xl text-[#C6C6C6]"
        >
          {{ data?.name }}
        </p>
        <p class="leading-[19.36px] text-sm ms:text-base text-[#C6C6C6]">
          {{ data?.position }}
        </p>
      </div>
    </div>
    <div class="flex justify-center">
      <img
        :src="getImageUrl(data.images)"
        alt="images"
        class="w-[103px] h-[103px] absolute rounded-[50%] bottom-[0] left-0 object-cover"
      />
      <img
        src="@/assets/static/elleps2.png"
        alt="circle"
        class="absolute top-[-50px] rounded-[50%] rotate-[180deg] right-[-80px] w-[190px] h-[190px]"
      />
    </div>
  </div>
</template>

<script setup lang="ts">
interface Props {
  data: {
    id: number;
    images: string;
    idea: string;
    name: string;
    position: string;
  };
}

defineProps<Props>();

function getImageUrl(name: string) {
  return new URL(`../../assets/fake-images/${name}`, import.meta.url).href;
}
</script>
