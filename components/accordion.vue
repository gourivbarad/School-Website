<script setup>
import { ref } from "vue";
const props = defineProps({
  accord: Object,
});
const toggle = ref(false);
function funcOpen() {
  toggle.value = !toggle.value;
  console.log(toggle.value, props.accord.id, "ki");
}
// const props = defineProps(["accord"]);
console.log(props.accord, "hi");
const array = ref([
  {
    id: 1,
    quest: `What are your hours and schedules?`,
    answer: `Praesent sapien massa, convallis a pellentesque nec, egestas non nisi. Nulla quis lorem ut libero malesuada feugiat. Curabitur arcu erat, accumsan id imperdiet et, porttitor at sem. Donec sollicitudin molestie malesuada.`,
    open: true,
  },
  {
    id: 2,
    quest: `What are your hours and schedules?`,
    answer: `Praesent sapien massa, convallis a pellentesque nec, egestas non nisi. Nulla quis lorem ut libero malesuada feugiat. Curabitur arcu erat, accumsan id imperdiet et, porttitor at sem. Donec sollicitudin molestie malesuada.`,
    open: false,
  },
  {
    id: 3,
    quest: `What are your hours and schedules?`,
    answer: `Praesent sapien massa, convallis a pellentesque nec, egestas non nisi. Nulla quis lorem ut libero malesuada feugiat. Curabitur arcu erat, accumsan id imperdiet et, porttitor at sem. Donec sollicitudin molestie malesuada.`,
    open: false,
  },
  {
    id: 4,
    quest: `What are your hours and schedules?`,
    answer: `Praesent sapien massa, convallis a pellentesque nec, egestas non nisi. Nulla quis lorem ut libero malesuada feugiat. Curabitur arcu erat, accumsan id imperdiet et, porttitor at sem. Donec sollicitudin molestie malesuada.`,
    open: false,
  },
  {
    id: 5,
    quest: `What are your hours and schedules?`,
    answer: `Praesent sapien massa, convallis a pellentesque nec, egestas non nisi. Nulla quis lorem ut libero malesuada feugiat. Curabitur arcu erat, accumsan id imperdiet et, porttitor at sem. Donec sollicitudin molestie malesuada.`,
    open: false,
  },
  {
    id: 6,
    quest: `What are your hours and schedules?`,
    answer: `Praesent sapien massa, convallis a pellentesque nec, egestas non nisi. Nulla quis lorem ut libero malesuada feugiat. Curabitur arcu erat, accumsan id imperdiet et, porttitor at sem. Donec sollicitudin molestie malesuada.`,
    open: false,
  },
]);
</script>

<template>
  <div class="flex flex-col">
    <div class="">
      <div
        @click="funcOpen()"
        class="flex justify-between bg-white p-8 w-full mt-4 rounded-t-3xl text-lg font-medium hover:text-slate-600"
      >
        <div>{{ props.accord.id + "." }} {{ props.accord.quest }}</div>
        <div>
          <svg
            xmlns="http://www.w3.org/2000/svg"
            width="24"
            height="24"
            viewBox="0 0 24 24"
            fill="none"
            stroke="currentColor"
            stroke-width="2"
            stroke-linecap="round"
            stroke-linejoin="round"
            class="fill-white hover:fill-slate-600"
          >
            <path d="M6 9l6 6l6 -6"></path>
          </svg>
        </div>
      </div>
      <div
        v-show="toggle == true"
        class="flex justify-between bg-white p-8 pt-0 w-full rounded-b-3xl text-lg font-medium text-black"
      >
        <p>
          {{ props.accord.answer }}
        </p>
      </div>
    </div>
  </div>
</template>
