<template>
  <section class="py-8">
    <div class="flex gap-4 items-center justify-center">
      <p class="text-white inline flex-shrink-0 leading-[19.36px]">
        <span class="text-[#FDF001] font-[400]"
          >02 <span class="px-1 pr-2 font-bold">|</span> </span
        >Mavjud kurslar !
      </p>
    </div>
    <div class="container">
      <h2
        class="font-['HuboSans'] leading-[34.81px] text-white font-semibold text-[28px] sm:text-[32px] text-center mt-4 sm:mt-4 max-w-[571px] mx-auto mb-6"
      >
        Bizda mavjud kurslar
      </h2>

      <div class="grid grid-cols-1 sm:grid-cols-2 dm:grid-cols-3 gap-[1.5rem]">
        <CoursesCard v-for="item in course" :key="item.id" :data="item" />
      </div>
    </div>
  </section>
</template>

<script setup lang="ts">
import CoursesCard from "@/components/card/CoursesCard.vue";
function getImageUrl(name: string) {
  return new URL(`../assets/team/${name}`, import.meta.url).href;
}

const course = [
  {
    id: 1,
    image: getImageUrl("frontend.png"),
    title: "Frontend",
    description:
      "Frontend kursimiz davomiyligi 6 oy bo'lib kurs yakunida 2 oy real loyihalar yordamida amaliyot o'tab beriladi.Darslar haftasiga 3 kun 2 saotdan o'tiladi.",
    moreContent: {
      title: "Kursimiz davomida quyidagi texnologiyalar o`tiladi",
      technology: [
        "Html",
        "Css",
        "Bootsrapt",
        "Tailwind css",
        "JavaScript",
        "React js",
        "Vue js",
      ],
    },
  },
  {
    id: 2,
    image: getImageUrl("backend.png"),
    title: "Backend",
    description:
      "Backend kursimiz davomiyligi 7 ou bo'lib kurs yakunida 2 oy real loyihalar davomida amaliyot o'tab beriladi. Darslari haftasiga 3 kun 2 soatdan o'tiladi.",
    moreContent: {
      title: "Kursimiz davomida quyidagi texnologiyalar o`tiladi",
      technology: [
        "Html",
        "Css",
        "Bootsrapt",
        "Tailwind css",
        "JavaScript",
        "React js",
        "Vue js",
      ],
    },
  },
  {
    id: 3,
    image: getImageUrl("flutter.jpg"),
    title: "Flutter",
    description:
      "  Flutter kursimiz davomiyligi 5 oy bo'lib kurs yakunida 2 oy real loyihalar yordamida amaliyot o'tab beriladi.Darslar haftasiga 3 kun 2 saotdan o'tiladi.",
    moreContent: {
      title: "Kursimiz davomida quyidagi texnologiyalar o`tiladi",
      technology: [
        "Html",
        "Css",
        "Bootsrapt",
        "Tailwind css",
        "JavaScript",
        "React js",
        "Vue js",
      ],
    },
  },
];
</script>
