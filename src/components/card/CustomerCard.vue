<template>
  <div>
    <div class="bg-[#F3F4F6] p-12 rounded-[10px] text-center">
      <img
        src="@/assets/images/icon/quote.svg"
        alt="icon"
        class="mx-auto h-[27px]"
      />
      <p class="mt-4 text-[#374151] font-normal leading-6">
        {{
          data.text
        }}
      </p>
    </div>
    <div class="mt-6 flex flex-col items-center">
      <img
        :src="getImageUrl(data.images)"
        alt="user image"
        class="w-12 h-12 rounded-[50%] object-cover mx-auto"
      />
      <p class="text-[#1F2937] font-semibold mt-2">Name</p>
      <p class="text-[#1F2937]">Designer</p>
    </div>
  </div>
</template>

<script setup lang="ts">
interface Props {
  data: {
    id: number;
    images: string;
    text: string;
  };
}

defineProps<Props>();

function getImageUrl(name: string) {
  return new URL(`../../assets/images/${name}.png`, import.meta.url).href;
}
</script>
