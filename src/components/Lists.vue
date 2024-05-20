<script setup>
import ListItem from "./ListItem.vue";
</script>

<template>
  <div class="container mx-auto py-32">
    <h2 class="text-5xl font-bold leading-[58.09px] text-center">
      List auto image subtract <br />
      thumbnail flatten auto mask
    </h2>
    <p class="mt-9 leading-[26.63px] text-center">
      Library object component device export prototype <br />
      selection line team
    </p>

    <div class="list-wrapper w-full flex flex-col items-center justify-center">
      <ListItem />
      <ListItem :opposite="true" />

      <div class="w-full mt-32">
        <img
          src="https://cdn.dribbble.com/userupload/3349890/file/original-54964eaa6cba4961bb0493df2f5e1249.png?resize=1024x768"
          alt=""
          class="mx-auto" />
      </div>

      <ListItem />
      <ListItem :opposite="true" />
    </div>
  </div>
</template>
