<script setup>
import Button from "./generics/Button.vue";
</script>
<template>
  <header>
    <div class="container mx-auto justify-between flex flex-wrap p-5 flex-col md:flex-row items-center px-40 z-10">
      <a class="flex title-font font-medium items-center text-gray-900 mb-4 md:mb-0 cursor-pointer z-10">
        <img src="../assets/icon/logo.svg" alt="" />
      </a>
      <nav class="flex items-center text-sm justify-center gap-9 ml-20 z-10">
        <router-link class="cursor-pointer">Mahsulot</router-link>
        <router-link class="cursor-pointer">Yechimlar</router-link>
        <router-link class="cursor-pointer">Tariflar</router-link>
        <router-link class="cursor-pointer">Izoh</router-link>
      </nav>
      <div class="flex gap-2">
        <Button>
          <span class="text-sm mr-2">Kirish</span>
        </Button>
        <Button class="bg-slate-100 py-2.5 px-5">
          <span class="flex items-center gap-2 text-sm">
            Boshlash
            <svg width="12" height="12" viewBox="0 0 12 12" fill="none" xmlns="http://www.w3.org/2000/svg">
              <path d="M4.5 9L7.5 6L4.5 3" stroke="#1F2937" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round" />
            </svg>
          </span>
        </Button>
      </div>
    </div>
  </header>
</template>

<style></style>
