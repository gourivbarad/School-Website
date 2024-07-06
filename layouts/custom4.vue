<script setup>
import Navbar from "../components/Navbar";
import Footer from "../components/Footer";
</script>
<template>
  <div>
    <Navbar />
    <div class="pt-10 pb-10">
      <slot />
    </div>

    <Footer />
  </div>
</template>
