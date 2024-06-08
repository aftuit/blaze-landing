<script setup>
import Button from "../components/generics/Button.vue";
</script>

<template>
  <div class="w-full lg:py-16 py-6 relative">
    <svg width="1161" height="839" viewBox="0 0 1161 839" fill="none" xmlns="http://www.w3.org/2000/svg" class="absolute -top-20 w-full">
      <g filter="url(#filter0_f_4_191)">
        <ellipse
          cx="308.564"
          cy="-103.309"
          rx="207"
          ry="507"
          transform="rotate(-35.6228 308.564 -103.309)"
          fill="#2158FF"
          fill-opacity="0.25" />
      </g>
      <defs>
        <filter
          id="filter0_f_4_191"
          x="-543.369"
          y="-1044.82"
          width="1703.87"
          height="1883.02"
          filterUnits="userSpaceOnUse"
          color-interpolation-filters="sRGB">
          <feFlood flood-opacity="0" result="BackgroundImageFix" />
          <feBlend mode="normal" in="SourceGraphic" in2="BackgroundImageFix" result="shape" />
          <feGaussianBlur stdDeviation="256" result="effect1_foregroundBlur_4_191" />
        </filter>
      </defs>
    </svg>
    <div class="container mx-auto lg:py-16 py-8 text-center relative lg:px-0 px-5">
      <div class="">
        <a href="tel:+998903380860" class="inline-flex md:text-base text-xs border rounded-3xl gap-1 items-center py-2 px-4 animate__animated animate__slideInDown">
          Hoziroq bog’laning:
          <span class="text-linear flex items-center gap-1 md:text-base text-xs">+998 (90) 338-08-60 
            <svg width="12" height="12" viewBox="0 0 12 12" fill="none" xmlns="http://www.w3.org/2000/svg">
              <path d="M2 6H10M10 6L7 3M10 6L7 9" stroke="#FF016C" stroke-linecap="round" stroke-linejoin="round" />
            </svg>
          </span>
        </a>

        <div class="mt-9 flex flex-col items-center animate__animated animate__slideInUp">
          <div class="card-shadow-sm p-2.5 ">
            <img src="../assets/icon/logo-dark-icon.svg" alt="" />
          </div>
          <span class="uppercase mt-2">Blaze</span>
        </div>
        <div class="flex flex-col items-center gap-2 mt-9 mb-16 justify-center max-w-screen-md mx-auto">
          <h2 class="lg:text-5xl text-3xl font-bold lg:leading-[58.09px] leading-[30px] animate__animated animate__slideInUp">Biznesingizda samarali boshqaruvga kafolat beramiz!</h2>
          <p class="md:mt-9 mt-5 leading-[26.63px] animate__animated animate__slideInUp">
            Delightful observability tools that turn your logs & monitoring into a secret weapon for shipping better software faster.
          </p>
          <Button class="group bg-primary hover:opacity-80 transition-all animate__animated animate__slideInUp duration-200 md:mt-16 mt-10 py-3 px-6 text-sm font-normal flex items-center gap-2"
            >Bepul sinab ko'rish
            <svg width="16" height="17" viewBox="0 0 16 17" fill="none" xmlns="http://www.w3.org/2000/svg" class="transition-all duration-150 group-hover:translate-x-1">
              <path
                d="M2.66669 8.5H13.3334M13.3334 8.5L9.33335 4.5M13.3334 8.5L9.33335 12.5"
                stroke="white"
                stroke-width="1.5"
                stroke-linecap="round"
                stroke-linejoin="round" />
            </svg>
          </Button>
        </div>
        <div class="container mx-auto lg:mb-32 mb-14 lg:px-40 animate__animated animate__slideInUp">
          <img src="../assets/img/header.png" alt="" class="mx-auto w-full" />
        </div>
      </div>
    </div>
  </div>
</template>
