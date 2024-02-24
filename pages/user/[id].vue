<script setup>
const route = useRoute();
console.log(route.params);
</script>

<template>
  <span>User ID:{{ $route.params.id }}</span>
</template>
