<script setup>
import { ref } from "vue";
// const name = ref("");
// const email = ref("");
// const phone = ref("");
// const prop = defineProps({
//   name: String,
// });
const route = useRoute();
console.log(route);
</script>

<template>
  <div class="flex pl-36 pr-36 mr-4 mt-12 mb-24 items-center justify-center">
    <div class="border border-red-200 p-8 bg-amber-200 rounded-lg">
      <div class="text-4xl font-medium">Your form is submitted !</div>
      <div class="flex flex-col p-2 items-center justify-center text-xl">
        <div>Name : {{ route.query.name }}</div>
        <div>Email : {{ route.query.email }}</div>
        <div>Phone : {{ route.query.phone }}</div>
      </div>
    </div>
  </div>
</template>
