<script setup>
import Navbar from "../components/Navbar";
import Footer from "../components/Footer";
</script>
<template>
  <div>
    <Navbar />
    <slot />
    <Footer />
  </div>
</template>
