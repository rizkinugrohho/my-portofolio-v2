<template>
  <div class="container mx-auto p-3 md:p-8">
    <div class="grid grid-cols-1 md:grid-cols-3 gap-5 auto-rows-fr fade-zoom-up">
      <article v-for="article in paginatedArticles" :key="article.id">
        <router-link :to="`/read/${article.slug}/${article.id}`" class="card bg-[#1e1e1f] border-[#383838] rounded-xl text-left text-white hover:bg-[#282828] flex flex-col h-full">
          <img :src="article.image" alt="thumbnail" class="card-image">
          <div class="p-4 flex-1 flex flex-col">
            <h1 class="text-lg md:text-lg text-sky-200 font-bold mb-5">{{ article.title }}</h1>
            <div class="text-xs mb-1 text-slate-400 italic">{{ article.date }}</div>
          </div>
        </router-link>
      </article>
    </div>

    <!-- Navigasi pagination -->
    <nav class="mt-4">
      <ul class="flex justify-center space-x-4">
        <li v-if="currentPage > 1">
          <button @click="changePage(currentPage - 1)" style="color: skyblue;">Previous</button>
        </li>
        <li v-for="page in totalPages" :key="page">
          <button @click="changePage(page)" :class="{ 'font-bold': page === currentPage, ' text-white': page === currentPage, 'text-skyblue': page !== currentPage }">{{ page }}</button>
        </li>
        <li v-if="currentPage < totalPages">
          <button @click="changePage(currentPage + 1)" style="color: skyblue;">Next</button>
        </li>
      </ul>
    </nav>

    <!-- Artikel List Component -->
    <ArticleList />
  </div>
</template>

<script>
import ArticleList from '@/components/ArticleList.vue';
import axios from "axios";

export default {
  data() {
    return {
      articles: [],
      currentPage: 1,
      perPage: 6,
    };
  },
  computed: {
    sortedArticles() {
      return this.articles.slice().sort((a, b) => new Date(b.date) - new Date(a.date));
    },
    paginatedArticles() {
      const startIndex = (this.currentPage - 1) * this.perPage;
      const endIndex = startIndex + this.perPage;
      return this.sortedArticles.slice(startIndex, endIndex);
    },
    totalPages() {
      return Math.ceil(this.sortedArticles.length / this.perPage);
    },
  },
  components: {
    ArticleList
  },
  mounted() {
    this.getArticles();
  },
  methods: {
    async getArticles() {
      try {
        const response = await axios.get('https://65cacf49efec34d9ed86526f.mockapi.io/blog');
        this.articles = response.data;
      } catch (error) {
        console.error("Error fetching articles:", error);
      }
    },
    changePage(page) {
      this.currentPage = page;
    },
  }
}
</script>

<style scoped>
.card {
  display: flex;
  flex-direction: column;
  height: 100%;
  transition: background-color 0.3s;
}
.card-image {
  width: 100%;
  height: 250px;
  object-fit: cover;
  border-radius: 0.5rem 0.5rem 0 0;
  transition: transform 0.3s ease; /* Tambahkan transition */
}
.card:hover .card-image {
  transform: scale(1.05); /* Efek zoom */
}
.card .p-4 {
  flex: 1;
  display: flex;
  flex-direction: column;
}
.card p {
  overflow: hidden;
  text-overflow: ellipsis;
  display: -webkit-box;
  -webkit-line-clamp: 3; /* Number of lines to show */
  -webkit-box-orient: vertical;
}
.auto-rows-fr {
  grid-auto-rows: 1fr;
}
@keyframes fadeZoomUp {
  0% {
    opacity: 0;
    transform: scale(0.5);
  }
  100% {
    opacity: 1;
    transform: scale(1);
  }
}
.fade-zoom-up {
  animation: fadeZoomUp 1s ease-in-out;
}
</style>
