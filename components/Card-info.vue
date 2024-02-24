<template>
  <div
    class="flex bg-slate-900 p-4 text-white text-xl m-20 items-center justify-center"
  >
    <div class="m-1 mr-3">
      <img :src="book.img" />
    </div>
    <div class="flex flex-col">
      <div class="pt-2">Author:{{ book.author }}</div>
      <div class="pt-2">
        {{ book.detail }}
      </div>
    </div>
  </div>
</template>
<script setup>
const props = defineProps({
  book: Object,
});
</script>
