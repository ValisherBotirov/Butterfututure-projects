<template>
  <article class="team_member cursor-pointer">
    <div class="team_member-image">
      <img :src="data.image" alt="" class="md:h-[230px] object-cover w-full" />
    </div>
    <div class="text-center font-['HuboSans']">
      <h4 class="mt-4 text-[#FFFFFFB2]">{{ data.name }}</h4>
      <p class="mt-2 text-[#A39FA2]">{{ data.position }}</p>
    </div>
    <div class="team_member-socials">
      <a href="#" target="_blank"
        ><i
          class="fa-brands fa-instagram text-white text-lg transition duration-300 hover:rotate-[360deg]"
        ></i
      ></a>
      <a href="#" target="_blank"
        ><i
          class="fa-brands fa-twitter text-white text-lg transition duration-300 hover:rotate-[360deg]"
        ></i
      ></a>
      <a href="#" target="_blank"
        ><i
          class="fa-brands fa-linkedin text-white text-lg transition duration-300 hover:rotate-[360deg]"
        ></i
      ></a>
    </div>
  </article>
</template>
<script setup lang="ts">
interface Props {
  data: {
    id: number;
    name: string;
    images: string;
    position: string;
    social?: {
      instagram: string;
      telegram: string;
      linkedln: string;
    };
  };
}

defineProps<Props>();
</script>

<style scoped>
.team_member {
  background-color: #1a1050;
  border-radius: 6px;
  padding: 2rem;
  border: 1px solid transparent;
  transition: all 400ms ease;
  position: relative;
  overflow: hidden;
}

.team_member:hover {
  background: transparent;
  border-color: #6c63ff;
}

.team_member-socials {
  position: absolute;
  top: 50%;
  transform: translateY(-50%);
  right: -100%;
  display: flex;
  flex-direction: column;
  background-color: #6c63ff;
  border-radius: 1rem 0 0 1rem;
  box-shadow: -2rem 0 2rem rgba(0, 0, 0, 0.3);
  transition: all 400ms ease;
}

.team_member:hover .team_member-socials {
  right: 0;
}

.team_member-socials a {
  padding: 0.5rem;
}

.team_member-image img {
  filter: saturate(0);
}

.team_member:hover img {
  filter: saturate(1);
}
</style>
