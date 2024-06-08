<script setup>
import ListItem from "./ListItem.vue";

import kinder1 from "../assets/img/kinder-1.png";
import kinder2 from "../assets/img/kinder-2.png";
import dental1 from "../assets/img/dental-1.png";
import dental2 from "../assets/img/dental-2.png";
import kinder3 from "../assets/img/kinder-3.png";

import { computed } from "vue";
const items = computed(() => {
  return {
    first: {
      title: "",
      description: "",
      image: kinder1,
    },
    second: {
      title: "",
      description: "",
      image: kinder2,
    },
    third: {
      title: "",
      description: "",
      image: dental1,
    },
    fourth: {
      title: "",
      description: "",
      image: dental2,
    },
  };
});
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
      <ListItem :img="items.first.image" />
      <ListItem :opposite="true" :img="items.second.image" />
    </div>
    <div class="w-full md:mt-32 mt-14 lg:px-0 px-5">
      <img
        :src="kinder3"
        alt=""
        class="mx-auto"
      />
    </div>
    <div
      class="list-wrapper w-full flex flex-col items-center justify-center lg:px-0 px-5"
    >
      <ListItem :img="items.third.image" />
      <ListItem :opposite="true" :img="items.fourth.image" />
    </div>
  </div>
</template>
