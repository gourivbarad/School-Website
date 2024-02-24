<template>
  <div>
    <div
      class="flex flex-col p-4 bg-amber-300 w-80 text-cyan-900 font-bold m-6 rounded-xl"
    >
      <div class="h-96">
        <img class="h-96 w-80" :src="book.img" />
        <!-- : colon is used for binding the properties -->
      </div>
      <div class="pt-2">Author:{{ book.author }}</div>
      <div class="pt-2 h-60">
        {{ book.detail }}
      </div>
      <div class="flex justify-center items-center">
        <Button :id="book.id" />
      </div>
    </div>
  </div>
</template>
<script setup>
const props = defineProps({
  book: Object,
});
</script>
