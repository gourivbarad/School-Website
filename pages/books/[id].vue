<script setup>
const route = useRoute();
const router = useRouter();
const bookId = route.params.id;
import { ref } from "vue";
let array = ref([
  {
    id: "1",
    img: "https://m.media-amazon.com/images/I/51+jk9Ja42L.jpg",
    author: "Mark Twain",
    detail:
      "The Adventures of Tom Sawyer is an 1876 novel by Mark Twain about a boy growing up along the Mississippi River. It is set in the 1840s in the town of St. Petersburg, which is based on Hannibal, Missouri, where Twain lived as a boy",
  },
  {
    id: "2",
    img: "https://m.media-amazon.com/images/I/91uMrXq+4RL._AC_UF1000,1000_QL80_.jpg",
    author: "Lewis Carrol",
    detail:
      "Alice's Adventures in Wonderland is an 1865 English children's novel by Lewis Carroll, a mathematics don at Oxford University. It details the story of a young girl named Alice who falls through a rabbit hole into a fantasy world of anthropomorphic creatures. It is seen as an example of the literary nonsense genre.",
  },
  {
    id: "3",
    img: "https://www.amarbooks.org/thumbs/1489711447.jpg",
    author: "Kazi Nasrul Islam",
    detail:
      "Agnibeena is the first poetry book written by Kazi Nazrul Islam, one of the most famous Bengali poet of the first half of the twentieth century. It was published in the month of Kartik, the Bengali year 1329. There are twelve poems in this book",
  },
  {
    id: "4",
    img: "https://cdn.kobo.com/book-images/90088bb7-3530-4de4-8873-7258d046ffa9/1200/1200/False/the-rime-of-the-ancient-mariner-32.jpg",
    author: "Coleridge",
    detail:
      "The Rime of the Ancient Mariner is the longest major poem by the English poet Samuel Taylor Coleridge, written in 1797–1798 and published in 1798 in the first edition of Lyrical Ballads. Some modern editions use a revised version printed in 1817 that featured a gloss",
  },
  {
    id: "5",
    img: "https://images-eu.ssl-images-amazon.com/images/I/81yx6h64TBL._AC_UL600_SR600,600_.jpg",
    author: "Babur",
    detail:
      "The Bāburnāma is the memoirs of Ẓahīr-ud-Dīn Muhammad Bābur, founder of the Mughal Empire and a great-great-great-grandson of Timur. It is written in the Chagatai language, known to Babur as Türki, the spoken language of the Timurids.",
  },
]);
const book = array.value.find((a) => {
  return a.id == bookId;
});
</script>
<template>
  <div class="flex pl-36 pr-36 mr-4 mt-12 pb-24 items-center justify-center">
    <span v-if="book == undefined"> Book Not Found </span>
    <Card-info v-else :book="book" />
  </div>
</template>
