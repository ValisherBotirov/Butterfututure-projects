<script setup lang="ts">
interface Props {
  image: string;
  id: number;
}

defineProps<Props>();
function getImageUrl(name: string) {
  return new URL(`../../assets/images/${name}.png`, import.meta.url).href;
}
</script>

<template>
  <div class="rounded-2xl">
    <img
      :src="getImageUrl(image)"
      alt="images"
      class="h-[216px] md:h-[488px] w-full  rounded-2xl object-cover"
    />
  </div>
</template>
