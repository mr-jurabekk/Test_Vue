<template>
  <header>

    <div class="wrapper w-full overflow-hidden">
      <Header></Header>
      <div class="dark:text-[#d0d2d6] text-3xl">
        hello world
      </div>
    </div>
  </header>

  <RouterView />
</template>

<script setup>
import { RouterLink, RouterView } from 'vue-router'
import MainPage from "./components/MainPage.vue";
import Header from "./components/layout/Header.vue";




</script>

