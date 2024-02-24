<script setup>
import { ref } from "vue";
const name = ref("");
const email = ref("");
const phone = ref("");
</script>

<template>
  <div
    class="flex pl-36 pr-36 mr-4 mt-12 mb-24 bg-gradient-to-r from-orange-50"
  >
    <div class="flex flex-col w-full pr-5 justify-center">
      <div
        class="w-60 text-center bg-violet-200 rounded-full p-2 pl-3 pr-3 mb-5"
      >
        Contact Us Today
      </div>
      <div
        class="text-7xl font-bold"
        style="font-family: 'Roboto Flex', sans-serif; color: #160041"
      >
        We'd love to hear from you
      </div>
      <div class="pt-2 text-xl pr-10">
        Praesent sapien massa, convallis a pellentesque nec, egestas non nisi.
        Mauris blandit aliquet elit, eget tincidunt nibh pulvinar a.
      </div>
    </div>
    <div
      class="flex flex-col p-16 w-full rounded-2xl m-4 bg-white"
      style="box-shadow: rgba(0, 0, 0, 0.35) 0px 5px 15px"
    >
      <div
        class="text-4xl font-bold"
        style="font-family: 'Roboto Flex', sans-serif; color: #160041"
      >
        Send us a message
      </div>
      <div class="text-lg pt-1">We'll get back to you within 24 hours.</div>
      <div class="flex flex-col">
        <p class="text-lg pt-4 font-medium text-slate-700">Name:{{ name }}</p>
        <input
          v-model="name"
          class="border border-slate-300 rounded-xl p-3 w-full"
        />
      </div>
      <div class="flex flex-col">
        <p class="text-lg pt-4 font-medium text-slate-700">Email</p>
        <input
          v-model="email"
          class="border border-slate-300 rounded-xl p-3 w-full"
        />
      </div>
      <div class="flex flex-col">
        <p class="text-lg pt-4 font-medium text-slate-700">Phone</p>
        <input
          v-model="phone"
          class="border border-slate-300 rounded-xl p-3 w-full"
        />
      </div>
      <div class="w-48">
        <NuxtLink
          :to="{
            path: 'contact/data',
            query: { name: name, email: email, phone: phone },
            params: { name: name, email: email, phone: phone },
          }"
        >
          <div
            class="w-auto rounded-3xl mt-6 p-2 text-base font-semibold transition ease-in-out delay-100 hover:-translate-y-1 hover:scale-110 duration-300"
            style="background-color: #f8d075"
          >
            <center class="text-xl">Submit</center>
          </div>
        </NuxtLink>
      </div>
    </div>
  </div>
</template>
