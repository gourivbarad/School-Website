<template>
  <div class="pl-32 pr-32">
    <div
      class="pt-8 pb-8 mt-14 text-4xl font-bold"
      style="background-color: #f0bf43"
    >
      <center class="text-white">Categories</center>
    </div>
    <div
      class="flex w-full justify-between items-center mt-9 mb-10 pl-20 pr-20"
    >
      <NuxtLink
        :to="{
          path: '/products/categories_m',
          query: { array: men },
        }"
        ><div
          class="p-3 text-base font-semibold transition ease-in-out delay-100 hover:-translate-y-1 hover:scale-110 duration-300"
          style="background-color: #f3dd61"
        >
          <center>Boy's clothing</center>
        </div></NuxtLink
      >
      <NuxtLink
        :to="{
          path: '/products/categories_w',
          query: { array: women },
        }"
      >
        <div
          class="p-3 text-base font-semibold transition ease-in-out delay-100 hover:-translate-y-1 hover:scale-110 duration-300"
          style="background-color: #f3dd61"
        >
          <center>Girl's colthing</center>
        </div></NuxtLink
      >
      <NuxtLink
        :to="{
          path: '/products/categories_e',
          query: { array: electronic },
        }"
      >
        <div
          class="p-3 text-base font-semibold transition ease-in-out delay-100 hover:-translate-y-1 hover:scale-110 duration-300"
          style="background-color: #f3dd61"
        >
          <center>Electronics</center>
        </div></NuxtLink
      >
    </div>
  </div>
</template>
<script setup>
const { data: products } = await useFetch("https://fakestoreapi.com/products");
const men = [];
const women = [];
const electronic = [];
products.value.forEach((i) => {
  console.log(i);
  console.log(i.category);
  if (i.category == "men's clothing") {
    men.push(i);
  }
  // console.log(men);
  else if (i.category == "women's clothing") {
    women.push(i.category);
  } else if (i.category == "electronics") {
    electronic.push(i.category);
  }
});
console.log(products);
</script>
