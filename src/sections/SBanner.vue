<template>
  <div class="relative sx:pb-4">
    <div class="container relative z-[20]">
      <div class="flex justify-between mt-20">
        <div class="max-w-[50%]">
          <p
            class="text-white sm:text-[50px] dm:text-[50px] font-semibold leading-130 sm:leading-[72.53px] font-hubo"
          >
            G'oyalaringizni birgalikda raqamli<span class="gradient-text">
              haqiqatga
            </span>
            aylantiramiz!
          </p>
          <SButton
            custom-class="!max-w-[200px]"
            class="mt-[50px] dm:mt-[70px]"
            @click="openModal = true"
          >
            {{ $t("connect") }}
          </SButton>
        </div>
        <div class="preson__animation">
          <img src="../assets/svg/person.svg" class="max-w-[70%]" alt="icon" />
        </div>

        <!-- <div
          class="mt-[77px] box-shadow mx-[20px] dm:mx-0 px-[20px] sm:px-[40px] dm:px-[52px] py-[25px] sm:py-[40px] dm:py-[48px] rounded-[15px]"
        >
          <p
            class="text-[#C6C6C6] text-center text-sm sm:text-base leading-[19.36px] font-[400]"
          >
            Bizning xizmatlarimiz va loyihangiz bo'yicha yechimlarimiz
            biznesingiz uchun cheksiz imkoniyatlar yaratadi va har qanday
            g'oyalaringizni ilgari surishingiz uchun zaminlikni ta'minlaydi!
          </p>
        </div> -->
        <!-- <div class="flex justify-center mt-[80px] ms:mt-[100px] dm:mt-[133px]">
          <a
            href="#blog-section"
            class="text-center cursor-pointer transition duration-300 group"
          >
            <p
              class="text-[#C6C6C6] group-hover:text-[#341289] text-sm sm:text-base transition duration-300"
            >
              {{ $t("more") }}
            </p>
            <img
              src="@/assets/icon/down-arrow.svg"
              alt="images"
              class="mx-auto mt-1"
            />
          </a>
        </div> -->
      </div>
    </div>

    <img
      src="@/assets/static/elleps2.png"
      alt="circle"
      class="absolute top-[-250px] right-0 w-[590px] h-[590px]"
    />
    <img
      src="@/assets/static/elleps2.png"
      alt="circle"
      class="absolute rounded-[50%] left-[-300px] bottom-[-20px] max-w-[50%] max-h-[80%]"
    />
    <SModal :is-open="openModal" @closeModal="(e) => (openModal = e)" />
  </div>
</template>
<script setup lang="ts">
import { ref } from "vue";
import SButton from "@/components/SButton.vue";
import SModal from "@/components/modal/SModal.vue";
const openModal = ref(false);
</script>

<style scoped>
.gradient-text {
  background-image: linear-gradient(265.79deg, #341289 -16.8%, #9949ff 89.61%);
  background-clip: text;
  -webkit-background-clip: text; /* Safari/Chrome */
  color: transparent;
}

.box-shadow {
  box-shadow: 0px -21px 30px 0px #7f43ff99;
  background: linear-gradient(180deg, #1b0f4e 0%, rgba(27, 15, 78, 0) 100%);
}

.font-hubo {
  font-family: "HuboSans";
}

.preson__animation {
  position: relative;
  animation: 3s infinite alternate example;
}
@keyframes example {
  0% {
    left: 0%;
  }
  50% {
    left: 5%;
  }
  100% {
    left: 0%;
  }
}
</style>
