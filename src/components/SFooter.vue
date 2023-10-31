<template>
  <div class="relative">
    <!-- <div class="mx-auto flex justify-center"></div> -->
    <div class="bg-[#130E29] w-full">
      <div class="container pt-8 pb-[30px]">
        <div class="parent__grid gap-2">
          <div>
            <div class="flex items-center gap-2">
              <div class="max-w-[50px] max-h-[50px] rounded-[50%]">
                <img
                  src="../assets/svg/logo-white.svg"
                  alt="logo"
                  class="py-1 px-1 w-full object-contain"
                />
              </div>
              <p class="text-white text-2xl">algaritm</p>
            </div>
            <div class="mt-7 dm:mt-[20px] flex items-center gap-6">
              <SocialBox
                v-for="(item, i) in socialLinks"
                :key="i"
                :icon="item.icon"
                :link="item.link"
              />
            </div>
          </div>
          <div class="mt-2 sm:mt-0 sm:flex-shrink-0">
            <p class="leading-[19.36px] font-semibold">
              {{ $t("our_services") }}
            </p>
            <div>
              <p
                v-for="(item, index) in services"
                :key="index"
                class="mt-[15px] text-[#C6C6C6] leading-[16.94px] text-sm"
              >
                {{ item?.name }}
              </p>
            </div>
          </div>
          <div class="mt-2 sm:mt-0 sm:flex-shrink-0">
            <p class="leading-[19.36px] font-semibold">
              {{ $t("our_lesson") }}
            </p>
            <div>
              <p
                v-for="(item, index) in lesson"
                :key="index"
                class="mt-[15px] text-[#C6C6C6] leading-[16.94px] text-sm"
              >
                {{ item?.name }}
              </p>
            </div>
          </div>
          <div class="mt-2 sm:mt-0 sm:flex-shrink-0">
            <p class="leading-[19.36px] font-semibold">
              {{ $t("connect") }}
            </p>
            <InfoSection
              icon="email"
              info="javokhir544@gmail.com"
              class="mt-[15px]"
            />
            <InfoSection icon="phone" info="(90) 915 25-26" class="mt-[15px]" />
          </div>
        </div>
      </div>
    </div>

    <div class="bg-[#191333] w-full">
      <div class="container text-center">
        <p class="text-[#C6C6C6] font-[400] text-sm pt-[14px] pb-[24px]">
          © 2023 algaritm.uz Barcha huquqlar himoyalangan
        </p>
      </div>
    </div>
    <SModal :is-open="openModal" @closeModal="(e) => (openModal = e)" />
  </div>
</template>

<script setup lang="ts">
import InfoSection from "@/components/InfoSection.vue";
import SocialBox from "@/components/SocialBox.vue";
import SModal from "@/components/modal/SModal.vue";
import { ref } from "vue";
const openModal = ref(false);
const socialLinks = [
  {
    link: "https://www.instagram.com/nodir__fs/",
    icon: "instagram",
  },
  {
    link: "https://t.me/algaritmacademy",
    icon: "telegram",
  },
  {
    link: "https://www.youtube.com/@algaritmuz/featured",
    icon: "youtube",
  },
];
const services = [
  {
    name: "Veb-sayt yasash",
  },
  {
    name: "Android apk yasash",
  },
  {
    name: "IOS apk yasash",
  },
  {
    name: "Telegiram bot yasash",
  },
];
const lesson = [
  {
    name: "Front end Development",
  },
  {
    name: "Back end Development",
  },
  {
    name: "iOS App Development",
  },
  {
    name: "Flutter App Development",
  },
  {
    name: "Android Development",
  },
];
</script>

<style scoped>
.connect-box {
  background: linear-gradient(261.54deg, #a69f29 -183.02%, #25166f 78.94%);
}
.parent__grid {
  color: #fff;
  display: flex;
  justify-content: space-between;
}

@media (max-width: 500px) {
  .parent__grid {
    display: block;
  }
}
@media (max-width: 768px) {
  .parent__grid {
    display: flex;
    flex-wrap: wrap;
  }
}
</style>
