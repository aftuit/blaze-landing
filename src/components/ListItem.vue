<script setup>
const props = defineProps({
  opposite: {
    type: Boolean,
    default: false,
  },
});
</script>

<template>
  <div
    class="flex lg:items-center items-start lg:gap-[114px] gap-[90px] md:mt-32 mt-14 lg:flex-row flex-col"
    :class="{ 'flex-row-reverse': opposite }"
  >
    <div>
      <div class="card-shadow-sm"></div>
      <h2 class="text-dark mt-9 md:leading-[38.73px] leading-[32px] md:text-[32px] text-3xl font-bold flex lg:flex-col flex-row">
        <span class="text-primary font-bold">Editor mask reesizing <br /> team background</span>
      </h2>
      <p class="mt-6 leading-[26.63px] flex lg:flex-col flex-row">
        <span>Component undo pixel pencil strike through.<br /> Layer pen bold slice stroke star</span>
      </p>
    </div>
    <div
      class="card-shadow rounded-3xl bg-slate-200 lg:w-[474px] h-[474px] w-full overflow-hidden"
    >
      <img
        src="https://cdn.dribbble.com/userupload/2993288/file/original-e0c3969a43acb896ba1435590b36824b.png?resize=1024x768&vertical=center"
        alt=""
        class="w-full h-full object-cover"
      />
    </div>
  </div>
</template>
