<script setup lang="ts">
  interface Props{
    title:string;
    description:string
  }

  defineProps<Props>()
</script>

<template>
  <div>
    <div class="flex items-center gap-2">
      <img src="@/assets/images/icon/right.svg" alt="icon">
      <p class="text-[#374151] font-semibold text-xl leading-5">{{ title }}</p>
    </div>
    <p class="mt-4 font-normal leading-6 text-[#374151]">{{
        description
      }}</p>
  </div>
</template>

