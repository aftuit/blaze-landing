<script setup>
const props = defineProps({
  opposite: {
    type: Boolean,
    default: false,
  },
});
</script>

<template>
  <div class="flex items-center gap-[114px] mt-32" :class="{'flex-row-reverse': opposite}">
    <div>
      <div class="card-shadow-sm"></div>
      <h2 class="text-dark mt-9 leading-[38.73px] text-[32px] font-bold">
        <span class="text-primary font-bold">Editor mask</span> reesizing <br> team background
      </h2>
      <p class="mt-6 leading-[26.63px]">Component undo pixel pencil <br> strikethrough. Layer pen bold slice stroke star</p>
    </div>
    <div class="card-shadow rounded-3xl bg-slate-200 w-[474px] h-[474px] overflow-hidden">
        <img src="https://cdn.dribbble.com/userupload/2993288/file/original-e0c3969a43acb896ba1435590b36824b.png?resize=1024x768&vertical=center" alt="" class="w-full h-full object-cover">
    </div>
  </div>
</template>
