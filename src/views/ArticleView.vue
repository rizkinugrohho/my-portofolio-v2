<template>
    <div class="w-full md:w-3/5 h-20 mx-auto md:mt-5">
      <div class="bg-white rounded-xl mx-3 p-5 md:p-10 md:mx-0">
        <div>
          <h1 class="text-xl md:text-4xl text-black text-left font-bold leading-relaxed">{{ title }}</h1>
          <div class="mt-3 text-left text-gray-800 text-sm">Published at <span>{{ date }}</span></div>
          <div class="h-[2px] w-20 my-5 md:my-10 bg-[#87ceeb] md:w-1/3 aos-init aos-animate mr-2"></div>
          <div class="relative w-full">
          <img :src="image" class="rounded-lg md:rounded-xl"
               alt="Thumbnail">
          </div>
        </div>
        <div class="text-left text-black mt-8" v-html="desc"></div>
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
      }
    },
    mounted() {
      this.getDetails();
    },
    methods: {
      async getDetails() {
        const id = this.route.params.id;
        axios.get('https://65cacf49efec34d9ed86526f.mockapi.io/blog/' + id)
          .then(response => {
            this.title = response.data.title;
            this.image = response.data.image;
            this.date = response.data.date;
            this.desc = response.data.desc;
          })
      }
    }
  }
  </script>
  
  <style scoped>
  /* Tambahkan gaya CSS tambahan jika diperlukan */
  </style>
