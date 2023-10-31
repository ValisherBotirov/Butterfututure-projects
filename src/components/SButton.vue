<template>
  <div
    class="cursor-pointer flex justify-center text-sm ms:text-base items-center py-3 bg-[#FF6600] text-white px-6 ms:px-4 rounded-[16px] font-medium transition duration-300 hover:bg-[#FF9900] hover:text-white active:scale-[0.95]"
    :class="customClass"
  >
    <slot></slot>
  </div>
</template>

<script setup lang="ts">
interface Props {
  customClass?: string;
}

defineProps<Props>();
</script>
