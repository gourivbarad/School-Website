<template>
  <div
    class="flex flex-wrap w-full items-center justify-center pl-36 pr-36 mr-4 mt-12 pb-24"
  >
    <div
      v-for="p in products"
      class="flex flex-col items-center justify-center border p-4 bg-amber-300 w-72 text-cyan-900 font-bold m-6 rounded-xl"
    >
      <!-- {{ p }} -->
      <NuxtLink :to="`products/${p.id}`">
        <div class="h-60">
          <img class="h-60 w-60" :src="p.image" />
          <!-- : colon is used for binding the properties -->
        </div>
        <div class="pt-2 h-24">{{ p.title }}</div>
      </NuxtLink>
    </div>
  </div>

  <!-- <div
    class="flex w-full items-center justify-center pl-36 pr-36 mr-4 mt-12 pb-24"
  >
    <div
      class="flex flex-col items-center justify-center border p-4 bg-amber-300 w-72 text-cyan-900 font-bold m-6 rounded-xl"
    >
       {{ p }} 
      <NuxtLink :to="`products/${cloth.id}`">
        <div class="h-60">
          <img class="h-60 w-60" :src="cloth.image" />
           : colon is used for binding the properties 
        </div>
        <div class="pt-2 h-24">{{ cloth.title }}</div>
      </NuxtLink>
    </div>
  </div> -->
</template>
<script setup>
const { data: products } = await useFetch("https://fakestoreapi.com/products");
console.log(products);
const props = defineProps({
  cloth: Object,
});
</script>
