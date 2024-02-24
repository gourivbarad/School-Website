<template>
  <div class="w-48">
    <NuxtLink :to="'books/' + id">
      <div
        class="w-auto rounded-3xl p-3 pl-8 pr-8 text-base font-semibold transition ease-in-out delay-100 hover:-translate-y-1 hover:scale-110 duration-300"
        style="background-color: #696212"
      >
        <center class="text-white">Read More</center>
      </div>
    </NuxtLink>
  </div>
</template>
<script setup>
const props = defineProps({
  id: String,
});
</script>
