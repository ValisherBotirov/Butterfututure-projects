<script setup lang="ts">
interface Props {
  title: string;
  description: string;
  imgName: string;
}

defineProps<Props>();

function getImageUrl(name: string) {
  return new URL(`../../assets/images/icon/${name}.svg`, import.meta.url).href;
}
</script>

<template>
  <div class="text-center">
    <div class="flex justify-center">
      <img :src="getImageUrl(imgName)" alt="icon" />
    </div>
    <div class="mt-4 max-w-[341px] mx-auto">
      <p class="text-[#374151] font-semibold text-xl leading-4">{{ title }}</p>
      <p class="mt-3 md:mt-4 font-normal leading-6 text-[#374151]">
        {{ description }}
      </p>
    </div>
  </div>
</template>

<style scoped></style>
