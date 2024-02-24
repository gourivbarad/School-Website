<template>
  <span v-if="products.id == undefined" class="pl-36 pr-36 text-xl text-center">
    <center>Product Not Found</center>
  </span>

  <div
    v-else
    :products="p"
    class="flex flex-wrap w-full items-center justify-center pl-36 pr-36 mr-4 mt-12 pb-24"
  >
    <div
      class="w-full flex items-center justify-center  p-4 bg-pink-100 border border-pink-300 text-cyan-900 font-bold m-6 rounded-xl"
    >
      <div class="h-80 w-1/2 flex justify-center m-1 items-center">
        <img class="h-80 rounded-xl" :src="product.image" />
        <!-- : colon is used for binding the properties -->
      </div>
      <div class="flex flex-col w-full ml-2">
        <div class="h-auto m-1">
          <b class="text-lg">Title :</b> {{ product.title }}
        </div>
        <div class="h-32">
          <b class="text-lg">Description</b> :{{ product.description }}
        </div>
        <div
          class="h-10 m-1 w-40 bg-green-50 rounded-xl flex justify-center items-center"
          style="box-shadow: rgba(0, 0, 0, 0.35) 0px 5px 15px"
        >
          <a href="#"><b class="text-lg">Price :</b></a>
          {{ product.price }}
        </div>
      </div>
    </div>
  </div>
</template>
<script setup>
// const props = defineProps({
//   cloth: Object,
// });
// console.log(cloth);
const route = useRoute();
console.log(route.params.id);
const ID = route.params.id;
const { data: products } = await useFetch("https://fakestoreapi.com/products/");
const url = "https://fakestoreapi.com/products/" + ID;
const { data: product } = await useFetch(url);

const p = product.value.find((P) => {
  return P.id == products.id;
});
</script>
