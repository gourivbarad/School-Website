<script setup>
const route = useRoute();
const curRoute = computed(() => {
  return route.fullPath;
});
</script>

<template>
  <div id="navbar-1">
    <div class="pl-32 pr-32 pt-6 flex justify-between p-3">
      <div>
        <a href="#"
          ><span
            ><img
              src="https://bright.tailwindawesome.com/_next/image?url=%2F_next%2Fstatic%2Fmedia%2Fbright-logo.095e684b.png&w=640&q=75"
              class="w-72" /></span
        ></a>
      </div>
      <div class="flex w-full">
        <div class="flex w-full justify-end">
          <span class="m-1">
            <svg
              xmlns="http://www.w3.org/2000/svg"
              width="24"
              height="24"
              viewBox="0 0 24 24"
              fill="none"
              stroke="currentColor"
              stroke-width="1"
              stroke-linecap="round"
              stroke-linejoin="round"
              class="mr-3 h-10 w-10 rounded-2xl bg-yellow-200 fill-yellow-200 p-1"
            >
              <path d="M9 11a3 3 0 1 0 6 0a3 3 0 0 0 -6 0"></path>
              <path
                d="M17.657 16.657l-4.243 4.243a2 2 0 0 1 -2.827 0l-4.244 -4.243a8 8 0 1 1 11.314 0z"
              ></path>
            </svg>
          </span>

          <div class="flex flex-col">
            <h5 class="font-semibold">Address</h5>
            <p class="w-full text-sm">
              958 McKinley Avenue Littleton, CO 80120
            </p>
          </div>
        </div>
        <div class="flex w-1/2 justify-end">
          <span class="m-1">
            <svg
              xmlns="http://www.w3.org/2000/svg"
              width="24"
              height="24"
              viewBox="0 0 24 24"
              fill="none"
              stroke="currentColor"
              stroke-width="1"
              stroke-linecap="round"
              stroke-linejoin="round"
              class="mr-3 h-10 w-10 rounded-2xl bg-purple-200 fill-purple-200 p-1"
            >
              <path
                d="M3 7a2 2 0 0 1 2 -2h14a2 2 0 0 1 2 2v10a2 2 0 0 1 -2 2h-14a2 2 0 0 1 -2 -2v-10z"
              ></path>
              <path d="M3 7l9 6l9 -6"></path>
            </svg>
          </span>

          <div class="flex flex-col">
            <h5 class="font-semibold">Email</h5>
            <p class="text-sm">hello@bright.com</p>
          </div>
        </div>
        <div class="flex w-1/2 justify-end">
          <span class="m-1">
            <svg
              xmlns="http://www.w3.org/2000/svg"
              width="24"
              height="24"
              viewBox="0 0 24 24"
              fill="none"
              stroke="currentColor"
              stroke-width="1"
              stroke-linecap="round"
              stroke-linejoin="round"
              class="mr-3 h-10 w-10 rounded-2xl bg-pink-200 fill-pink-200 p-1"
            >
              <path
                d="M5 4h4l2 5l-2.5 1.5a11 11 0 0 0 5 5l1.5 -2.5l5 2v4a2 2 0 0 1 -2 2a16 16 0 0 1 -15 -15a2 2 0 0 1 2 -2"
              ></path>
            </svg>
          </span>

          <div class="flex flex-col">
            <h5 class="font-semibold">Phone</h5>
            <p class="text-sm">+1-202-555-0132</p>
          </div>
        </div>
      </div>
    </div>
    <div class="border-2 border-gray-100 border-b-slate-300 ml-32 mr-32"></div>
    <div class="pl-32 pr-32 mt-7 flex justify-between">
      <div class="flex w-full">
        <div class="flex flex-col">
          <div
            class="mr-9 text-lg font-medium text-gray-600 dark:text-white hover:border-b-4 border-yellow-500"
            :class="route.fullPath == '/' ? 'border-b-4' : ''"
          >
            <NuxtLink to="/">Home </NuxtLink>
          </div>
        </div>

        <div class="flex flex-col">
          <div
            class="mr-9 text-lg font-medium text-gray-600 dark:text-white hover:border-b-4 border-yellow-500"
            :class="route.fullPath == '/about' ? 'border-b-4' : ''"
          >
            <NuxtLink to="/about"><a>About</a></NuxtLink>
          </div>
        </div>

        <!-- <div
          class="mb-0 pb-0 mr-9 text-lg font-medium text-gray-600  hover:border-b-4 border-yellow-500"
        >
          <NuxtLink to="/about">About</NuxtLink>
        </div>
         <span
            class="h-1 hover:bg-gradient-to-r from-[#fbde9b] to-[#f8d075] w-14 rounded"
          ></span
        > -->

        <div class="flex flex-col">
          <div
            class="mr-9 text-lg font-medium text-gray-600 dark:text-white hover:border-b-4 border-yellow-500"
            :class="route.fullPath == '/staff' ? 'border-b-4' : ''"
          >
            <NuxtLink to="/staff">Staff</NuxtLink>
          </div>
        </div>

        <div class="flex flex-col">
          <div
            class="mr-9 text-lg font-medium text-gray-600 dark:text-white hover:border-b-4 border-yellow-500"
            :class="route.fullPath == '/class' ? 'border-b-4' : ''"
          >
            <NuxtLink to="/class">Classes</NuxtLink>
          </div>
        </div>

        <div class="flex flex-col">
          <div
            class="mr-9 text-lg font-medium text-gray-600 dark:text-white hover:border-b-4 border-yellow-500"
            :class="route.fullPath == '/blog' ? 'border-b-4' : ''"
          >
            <NuxtLink to="/blog" exact>Blogs</NuxtLink>
          </div>
        </div>

        <div class="flex flex-col">
          <div
            class="mr-9 text-lg font-medium text-gray-600 dark:text-white hover:border-b-4 border-yellow-500"
            :class="route.fullPath == '/books' ? 'border-b-4' : ''"
          >
            <NuxtLink to="/books">Books</NuxtLink>
          </div>
        </div>

        <div class="flex flex-col">
          <div
            class="mr-9 text-lg font-medium text-gray-600 dark:text-white hover:border-b-4 border-yellow-500"
            :class="route.fullPath == '/contact' ? 'border-b-4' : ''"
          >
            <NuxtLink to="/contact">Contact</NuxtLink>
          </div>
        </div>

        <div class="flex flex-col">
          <div
            class="mr-9 text-lg font-medium text-gray-600 dark:text-white hover:border-b-4 border-yellow-500"
            :class="route.fullPath == '/products' ? 'border-b-4' : ''"
          >
            <NuxtLink to="/products">Products</NuxtLink>
          </div>
        </div>
      </div>
      <div class="w-48">
        <NuxtLink to="/contact">
          <div
            class="w-auto rounded-3xl p-3 pl-8 pr-8 text-base font-semibold transition ease-in-out delay-100 hover:-translate-y-1 hover:scale-110 duration-300"
            style="background-color: #f8d075"
          >
            <center>Enroll Today</center>
          </div>
        </NuxtLink>
      </div>
    </div>
  </div>
</template>
