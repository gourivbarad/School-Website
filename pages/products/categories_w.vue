<template>
  <ProductCard  v-for="item in women" :cloth="item" />

</template>
<script setup>
const props = defineProps({
  women: Object,
});
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
