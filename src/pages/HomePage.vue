<template>
  <div>
    <SBanner id="main-section"  />
    <!--    <SBlock id="blog-section" />-->
    <STeam />
    <SClustomer id="customer-section" />
    <SContact class="!mb-[100px]" />
  </div>
</template>
<script setup lang="ts">
import SBanner from "@/sections/SBanner.vue";
import SClustomer from "@/sections/SClustomer.vue";
import SContact from "@/sections/SContact.vue";
import STeam from "@/sections/STeam.vue";
</script>
