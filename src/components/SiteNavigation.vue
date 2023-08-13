<template>
  <header class="sticky top-0 bg-weather-primary shadow-lg">
    <nav
      class="container py-6 flex flex-col sm:flex-row items-center gap-4 text-white"
    >
      <RouterLink :to="{ name: 'home' }">
        <div class="flex items-center gap-3">
          <i class="fa-solid fa-cloud text-2xl"></i>
          <span class="text-2xl">VVueather</span>
        </div>
      </RouterLink>
      <div class="flex flex-1 gap-3 justify-end">
        <i
          @click="toggleModal"
          class="fa-solid fa-info hover:text-weather-secondary text-xl cursor-pointer duration-200"
        ></i>
        <i
          class="fa-solid fa-plus hover:text-weather-secondary text-xl cursor-pointer duration-200"
        ></i>
      </div>
      <BaseModal :modalActive="modalActive" @close-modal="toggleModal">
        <h1 class="text-black">About</h1>
        <p class="text-black mt-5">
          Lorem ipsum dolor sit, amet consectetur adipisicing elit. Tempora quam
          exercitationem illo necessitatibus consequatur. Architecto officiis
          aut quam alias saepe vitae error! Facere, fuga exercitationem!
          Veritatis dolor beatae, praesentium, a eos ratione labore qui
          exercitationem atque hic quia, deserunt tenetur.
        </p>
      </BaseModal>
    </nav>
  </header>
</template>

<script setup>
import { RouterLink } from "vue-router";
import BaseModal from "./BaseModal.vue";
import { ref } from "vue";

const modalActive = ref(null);
const toggleModal = () => {
  modalActive.value = !modalActive.value;
};
</script>

<style lang="scss" scoped></style>
