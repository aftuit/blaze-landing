<script setup>
import Button from "./generics/Button.vue";
import { onMounted, ref } from "vue";
const scrolled = ref(false);
const open = ref(false);

onMounted(() => {
  window.addEventListener("scroll", () => {
    scrolled.value = window.scrollY > 50;
  });
});
</script>
<template>
  <header
    class="h-[72px] flex items-center sticky top-0 z-10 transition-colors duration-300"
    :class="{ 'bg-white shadow border-bottom': scrolled }"
  >
    <div
      class="container mx-auto justify-between flex flex-row items-center lg:px-40 sm:px-10 px-5 z-10"
    >
      <a
        class="flex title-font font-medium items-center text-gray-900 md:mb-0 cursor-pointer z-10"
      >
        <img src="../assets/icon/logo.svg" alt="logo" width="100" />
      </a>
      <nav
        class="lg:flex hidden items-center text-sm justify-center gap-9 xl:ml-20 z-10"
      >
        <router-link class="cursor-pointer">Mahsulot</router-link>
        <router-link class="cursor-pointer">Yechimlar</router-link>
        <router-link class="cursor-pointer">Tariflar</router-link>
        <router-link class="cursor-pointer">Izoh</router-link>
      </nav>
      <div class="lg:flex hidden gap-2">
        <Button>
          <span class="text-sm mr-2">Kirish</span>
        </Button>
        <Button class="bg-slate-100 py-2.5 px-5">
          <span class="flex items-center gap-2 text-sm">
            Boshlash
            <svg
              width="12"
              height="12"
              viewBox="0 0 12 12"
              fill="none"
              xmlns="http://www.w3.org/2000/svg"
            >
              <path
                d="M4.5 9L7.5 6L4.5 3"
                stroke="#1F2937"
                stroke-width="1.5"
                stroke-linecap="round"
                stroke-linejoin="round"
              />
            </svg>
          </span>
        </Button>
      </div>
      <div class="lg:hidden block cursor-pointer">
        <div id="nav-icon3" :class="{ open: open }" @click="open = !open">
          <span></span>
          <span></span>
          <span></span>
          <span></span>
        </div>
      </div>
    </div>
  </header>

  <!-- mobile sidebar -->
  <!-- <div class="">
    <div class="lg:hidden" v-if="open">
      <div class="bg-white h-screen w-full fixed top-0 left-0 z-50">
        <div class="flex flex-col items-center justify-center h-full">
          <router-link class="cursor-pointer">Mahsulot</router-link>
          <router-link class="cursor-pointer">Yechimlar</router-link>
          <router-link class="cursor-pointer">Tariflar</router-link>
          <router-link class="cursor-pointer">Izoh</router-link>
          <Button>
            <span class="text-sm mr-2">Kirish</span>
          </Button>
          <Button class="bg-slate-100 py-2.5 px-5">
            <span class="flex items"></span>
          </Button>
        </div>
      </div>
    </div>
  </div> -->
</template>

<style scoped>
#nav-icon3 {
  width: 35px;
  height: 30px;
  position: relative;
  -webkit-transform: rotate(0deg);
  -moz-transform: rotate(0deg);
  -o-transform: rotate(0deg);
  transform: rotate(0deg);
  -webkit-transition: 0.5s ease-in-out;
  -moz-transition: 0.5s ease-in-out;
  -o-transition: 0.5s ease-in-out;
  transition: 0.5s ease-in-out;
  cursor: pointer;
  transform: scale(0.75);
}
#nav-icon3 span {
  display: block;
  position: absolute;
  height: 4px;
  width: 100%;
  background: #383636;
  border-radius: 9px;
  opacity: 1;
  left: 0;
  -webkit-transform: rotate(0deg);
  -moz-transform: rotate(0deg);
  -o-transform: rotate(0deg);
  transform: rotate(0deg);
  -webkit-transition: 0.25s ease-in-out;
  -moz-transition: 0.25s ease-in-out;
  -o-transition: 0.25s ease-in-out;
  transition: 0.25s ease-in-out;
}

/* Icon 3 */

#nav-icon3 span:nth-child(1) {
  top: 5px;
}
#nav-icon3 span:nth-child(2),
#nav-icon3 span:nth-child(3) {
  top: 14px;
  width: 70%;
}

#nav-icon3 span:nth-child(4) {
  top: 23px;
}

#nav-icon3.open span:nth-child(1) {
  top: 10px;
  width: 0%;
  left: 50%;
}

#nav-icon3.open span:nth-child(2) {
  width: 100%;
  -webkit-transform: rotate(45deg);
  -moz-transform: rotate(45deg);
  -o-transform: rotate(45deg);
  transform: rotate(45deg);
}

#nav-icon3.open span:nth-child(3) {
  width: 100%;
  -webkit-transform: rotate(-45deg);
  -moz-transform: rotate(-45deg);
  -o-transform: rotate(-45deg);
  transform: rotate(-45deg);
}

#nav-icon3.open span:nth-child(4) {
  top: 10px;
  width: 0%;
  left: 50%;
}
</style>
