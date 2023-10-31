<template>
  <div>
    <SBanner id="main-section" class="md:h-[84vh]" />
    <!-- <SAbout id="about-section" /> -->
    <SService id="service-section" />
    <SCourses />
    <!--    <SBlock id="blog-section" />-->
    <STeam />
    <SClustomer id="customer-section" />
    <SContact class="!mb-[100px]" />
  </div>
</template>
<script setup lang="ts">
import SBanner from "@/sections/SBanner.vue";
import SService from "@/sections/SService.vue";
// import SAbout from "@/sections/SAbout.vue";
// import SBlock from "@/sections/SBlock.vue";
import SClustomer from "@/sections/SClustomer.vue";
import SContact from "@/sections/SContact.vue";
import STeam from "@/sections/STeam.vue";
import SCourses from "@/sections/SCourses.vue";
</script>
