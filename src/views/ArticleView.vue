<template>
    <div class="w-full md:w-3/5 h-20 mx-auto md:mt-5">
      <div class="bg-white rounded-xl mx-3 p-5 md:p-10 md:mx-0">
        <div>
          <h1 class="text-xl md:text-4xl text-black text-left font-bold leading-relaxed">{{ title }}</h1>
          <div class="mt-3 text-left text-gray-800 text-sm">Published at <span>{{ date }}</span></div>
          <div class="h-[2px] w-20 my-5 md:my-10 bg-[#87ceeb] md:w-1/3 aos-init aos-animate mr-2"></div>
          <div>
            <div class="relative w-full" style="padding-top: 50%;">
              <img :src="image || 'https://placekitten.com/200/200'" class="absolute top-0 left-0 rounded-lg w-full h-full object-cover" alt="Thumbnail">
            </div>
          </div>
          <div class="text-left text-black mt-8" v-html="content"></div>
        </div>
      </div>
    </div>
  </template>
  
  <script>
  import axios from 'axios';
  import { useRoute } from 'vue-router';
  
  export default {
    data() {
      return {
        route: useRoute(),
        title: '',
        image: '',
        date: '',
        content: '',
      };
    },
    mounted() {
      this.getDetails();
    },
    methods: {
      async getDetails() {
        const id = this.route.params.id;
        const apiKey = '12ef1beae8474690aac22675a4c6b96f';
        const apiUrl = 'https://newsapi.org/v2/everything'; // Ganti dengan endpoint everything
  
        try {
          const response = await axios.get(apiUrl, {
            params: {
              apiKey,
              q: id,
            },
          });
  
          const article = response.data.articles[0];
          this.title = article.title;
          this.image = article.urlToImage;
          this.date = article.publishedAt;
          this.content = article.content;
        } catch (error) {
          console.error('Error fetching article details:', error);
        }
      },
    },
  };
  </script>
  
  <style scoped>
  /* Tambahkan gaya CSS sesuai kebutuhan */
  </style>