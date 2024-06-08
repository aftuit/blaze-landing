<script setup>
import ListItem from "./ListItem.vue";
</script>

<template>
  <div class="container mx-auto md:py-32 py-10">
    <h2
      class="md:text-5xl text-3xl font-bold md:leading-[58.09px] leading-[40px] text-center"
    >
      List auto image subtract <br />
      thumbnail flatten auto mask
    </h2>
    <p class="md:mt-9 mt-5 leading-[26.63px] text-center">
      Library object component device export prototype <br />
      selection line team
    </p>

    <div
      class="list-wrapper w-full flex flex-col items-center justify-center lg:px-0 px-5"
    >
      <ListItem />
      <ListItem :opposite="true" />
    </div>
    <div class="w-full md:mt-32 mt-14 lg:px-0 px-5">
      <img
        src="https://cdn.dribbble.com/userupload/3349890/file/original-54964eaa6cba4961bb0493df2f5e1249.png?resize=1024x768"
        alt=""
        class="mx-auto"
      />
    </div>
    <div class="list-wrapper w-full flex flex-col items-center justify-center lg:px-0 px-5">
      <ListItem />
      <ListItem :opposite="true" />
    </div>
  </div>
</template>
