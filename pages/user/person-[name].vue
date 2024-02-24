<script setup>
const route = useRoute();
console.log(route.params);
</script>
<template>
  <div>User name:{{ $route.params.name }}</div>
  <!-- <div>User id:{{ $route.params.id }}</div>
  <div>User dept:{{ $route.params.dept }}</div> -->
</template>
