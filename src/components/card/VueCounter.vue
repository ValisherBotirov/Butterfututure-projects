<script setup lang="ts">
interface Props {
  count: number;
  text: string;
}

defineProps<Props>();
</script>

<template>
  <div class="max-w-[164px]">
    <vue3-autocounter
      class="font-[800] text-4xl text-[#1F2937]"
      ref="counter"
      :startAmount="0"
      :endAmount="count"
      :duration="4"
      suffix="K"
      separator=" "
      :autoinit="true"
    />
    <p class="mt-2 font-medium text-[#374151] leading-4 text-sm">
      {{ text }}
    </p>
  </div>
</template>
