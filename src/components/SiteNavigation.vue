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
          class="fa-solid fa-info hover:text-weather-secondary text-xl cursor-pointer duration-200"
        ></i>
        <i
          class="fa-solid fa-plus hover:text-weather-secondary text-xl cursor-pointer duration-200"
        ></i>
      </div>
    </nav>
  </header>
</template>

<script setup>
import { RouterLink } from "vue-router";
</script>

<style lang="scss" scoped></style>
