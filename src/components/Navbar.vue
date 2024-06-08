<script setup>
import Button from "./generics/Button.vue";
import { onMounted, ref, computed } from "vue";
const scrolled = ref(false);
const open = ref(false);

const links = computed(() => [
  { name: "Mahsulot", path: "/" },
  { name: "Yechimlar", path: "/" },
  { name: "Tariflar", path: "/" },
  { name: "Izoh", path: "/" },
]);

onMounted(() => {
  window.addEventListener("scroll", () => {
    scrolled.value = window.scrollY > 50;
  });
});
</script>
<template>
  <header
    class="h-[72px] flex items-center sticky top-0 z-10 transition-colors duration-300"
    :class="{ 'bg-white shadow border-bottom': scrolled, 'bg-white': open }"
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
        <router-link
          :to="link.href"
          v-for="link in links"
          :key="link.href"
          class="cursor-pointer"
          >{{ link.name }}</router-link
        >
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
      <div
        class="lg:hidden block cursor-pointer border p-1 rounded-md relative"
        @click="open = !open"
      >
        <div id="nav-icon3" :class="{ open: open }" >
          <span></span>
          <span></span>
          <span></span>
          <span></span>
        </div>
      </div>
    </div>
  </header>

  <!-- mobile sidebar should be as a dropdown, and displays bottom of the burger icon -->
  <div
    class="fixed top-[72px] w-full h-[43vh] bg-white z-20 transition-all duration-150 ease-in shadow-md flex flex-col px-5 py-10"
    :class="open ? 'right-0' : '-right-full'"
  >
    <div class="flex flex-col items-start gap-2">
      <router-link
        :to="link.href"
        v-for="link in links"
        :key="link.href"
        class="cursor-pointer text-base hover:text-[#2158FF] transition-colors duration-100 w-full flex justify-between items-center group"
        > {{ link.name }}
        <svg
          width="19"
          height="19"
          viewBox="0 0 24 24"
          fill="#474646d1"
          xmlns="http://www.w3.org/2000/svg"
          class="group-hover:fill-[#2158FF] transition-all duration-100"
        >
          <path
            d="M14.293 15.2929C13.9025 15.6834 13.9025 16.3166 14.293 16.7071C14.6835 17.0976 15.3167 17.0976 15.7072 16.7071L19.7072 12.7071C20.0977 12.3166 20.0977 11.6834 19.7072 11.2929L15.7072 7.29289C15.3167 6.90237 14.6835 6.90237 14.293 7.29289C13.9025 7.68342 13.9025 8.31658 14.293 8.70711L16.5859 11H5C4.44771 11 4 11.4477 4 12C4 12.5523 4.44771 13 5 13H16.5859L14.293 15.2929Z"
          />
        </svg>
      </router-link>
    </div>
    <div class="flex gap-2 mt-auto w-full justify-end">
      <Button class="hover:bg-slate-100 py-2.5 px-5 mr-2">
        <span class="text-sm">Kirish</span>
      </Button>
      <Button class="bg-slate-100 hover:bg-slate-200 py-2.5 px-5">
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
  </div>
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
