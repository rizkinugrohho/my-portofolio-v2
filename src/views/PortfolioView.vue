<script>
export default {
  data() {
    return {
      activeTab: 1,
      items: [
        {
          id: 1,
          name: 'AI-Driven Web3 Crypto Mine SaintAI',
          imageUrl: 'saint',
          status: 'Website to convert productive generative AI computing power into cryptocurrency mining.',
          tech: 'Python, Vue Js, Tailwind, Css',
          github: 'https://saint-mia.onrender.com/',
          demo: 'https://saint-mia.onrender.com/',
          category: 'web'
        },
        {
          id: 2,
          name: 'Laravel-Vue E-Commerce',
          imageUrl: 'laravel-vue',
          status: 'E-commerce application built with Laravel, Vue.js, Tailwind.css and Alpine.js.',
          tech: 'Laravel, Vue Js, Tailwind, Alphine Js, Html, Css',
          github: 'https://github.com/rizkinugrohho/laravel-vue',
          demo: 'https://github.com/rizkinugrohho/laravel-vue',
          category: 'web'
        },
        {
          id: 3,
          name: 'Nike Landing Page',
          imageUrl: 'landingpage',
          status: 'Discover stylish Nike arrivals, quality comfort, and innovation for your active life.',
          tech: 'Vite, React, Tailwind, Javascript, Html, Css',
          github: 'https://github.com/rizkinugrohho/nike-landing-page',
          demo: 'https://rizkinugrohho.github.io/nike-landing-page/',
          category: 'web'
        },
        {
          id: 4,
          name: 'Booking Hotel Web',
          imageUrl: 'portfolio-hotel',
          status: 'A Simple Hotel Booking Website. This project aims to create a user-friendly platform for booking hotel accommodations.',
          tech: 'Php, Ajax, Javascript, Boostrap',
          github: 'https://github.com/rizkinugrohho/booking-hotel',
          demo: 'null',
          category: 'web'
        },
        {
          id: 5,
          name: 'Personal Website',
          imageUrl: 'portfolio_v2',
          status: 'My personal website, I created this website to display my profile, skills and projects. As well as my place to try new technology.',
          tech: 'VueJS 3, NodeJs, Tailwind',
          github: 'https://github.com/rizkinugrohho/my-portofolio-v2',
          demo: 'rizkinugroho.netlify.app',
          category: 'web'
        },
        {
          id: 6,
          name: 'Weather App',
          imageUrl: 'weatherapp',
          status: 'Android Mobile Application that shows todays weather and weather forecast for the next 5 days in various cities and countries.',
          tech: 'Kotlin, RestAPi, Android',
          github: 'https://github.com/rizkinugrohho/MobileApplication_Weather-App',
          demo: 'https://github.com/rizkinugrohho/MobileApplication_Weather-App',
          category: 'mobile'
        },
        {
          id: 7,
          name: 'Mandiri News App',
          imageUrl: 'mandiri',
          status: 'Challenge from Bank Mandiri - Creating an Android Mobile Application that displays a list of news using API from https://newsapi.org',
          tech: 'Kotlin, RestAPi, Android',
          github: 'https://github.com/rizkinugrohho/MobileApplication_MandiriNews',
          demo: 'https://github.com/rizkinugrohho/MobileApplication_MandiriNews',
          category: 'mobile'
        },
        {
          id: 8,
          name: 'Progresive Web App React Js',
          imageUrl: 'webapp',
          status: 'a progressive e-commerce web application, which has Push Notification Features, App Banner (Add to Home Screen), Splash screen on the application, Service Worker with Workbox JS.',
          tech: 'ReactJs, NodeJs, Tailwind',
          github: 'https://github.com/rizkinugrohho/Web_Apps_With_React_Js',
          demo: 'https://web-apps-phi.vercel.app/',
          category: 'web'
        },
        {
          id: 9,
          name: 'Bookshelf App',
          imageUrl: 'bookshelf',
          status: 'allows users to search for books, view book details, leave reviews, add books to favorites, and view example categories of books.',
          tech: 'Javascript',
          github: 'https://github.com/rizkinugrohho/bookshelf-apps',
          demo: 'bookshelf-appli.netlify.app/',
          category: 'web'
        }
      ],
      filteredItems: [] // Daftar proyek yang telah difilter
    };
  },
  methods: {
    filterByCategory(category) {
      if (category === 'all') {
        this.filteredItems = this.items; // Menampilkan semua proyek
      } else {
        this.filteredItems = this.items.filter(item => item.category === category); // Filter berdasarkan kategori
      }
    }
  },
  mounted() {
    this.filteredItems = this.items; // Set daftar proyek awal saat komponen dimuat
  }
};
</script>
<template>
  <div class="px-5 py-5 md:px-12 md:py-10 text-left text-sky-50 mx-3">
    <article data-page="about">
      <header>
        <div
          class="text-2xl font-bold text-white mb-10 fadein-bot title-section flex items-center justify-center flex-col">
          <!-- <div class="h-[1px] w-10 bg-sky-200 md:w-20 aos-init aos-animate"></div> -->
          <h4>Past Project Experience</h4>
          <h4 class="text-base font-normal text-transparent bg-clip-text bg-gradient-to-r from-slate-100 to-sky-300">
            Explore the projects I've worked on so far</h4>
          <div class="filter-container">
            <button @click="filterByCategory('all')" class="filter-btn">All</button>
            <button @click="filterByCategory('web')" class="filter-btn">Web</button>
            <button @click="filterByCategory('mobile')" class="filter-btn">Mobile</button>
          </div>
        </div>

      </header>
      <section>
        <div>
          <div
            class="grid grid-cols-1 gap-4 pb-32 md:grid-cols-3 md:gap-3 xl:grid-cols-3 xl:gap-3 2xl:gap-5 fade-zoom-in">
            <div v-for="item in filteredItems" :key="item.id">
              <div
                class="item-card flex flex-col items-center gap-2 rounded bg-[#1e1e1f] hover:bg-[#282828] border border-[#383838] rounded-xl text-sky-50 md:gap-3 px-5 py-5 lg:px-5 ">
                <div class="flex h-12 w-12 items-center justify-center p-0 h-full w-full lg:p-0 zoom-in">
                  <img alt="HTML" loading="lazy" decoding="async" data-nimg="1"
                    class="drop-shadow-xl rounded rounded-xl" :src="'/img/portfolio-' + item.imageUrl + '.png'">
                </div>
                <div class="w-full flex flex-col gap-2 items-center text-sm md:text-base lg:text-lg">
                  <div class="title-text font-medium text-secondary">{{ item.name }}
                  </div>
                  <div class="w-full text-left text-[10px] text-[#c1c1c1] md:text-xs lg:text-sm">
                    {{ item.status }}</div>
                  <div class="w-full mt-4 text-normal text-sm text-left text-sky-200">
                    {{ item.tech }}
                  </div>
                  <div class="w-full flex justify-end">
                    <div class="flex cursor-pointer items-end gap-2 text-primary">
                      <a v-if="item.github !== 'null'" :href="item.github" target="_blank" rel="noreferrer"
                        title="View github repository" class="transition-all hover:text-accent">
                        <svg stroke="currentColor" fill="none" stroke-width="2" viewBox="0 0 24 24"
                          stroke-linecap="round" stroke-linejoin="round" height="16" width="16"
                          xmlns="http://www.w3.org/2000/svg">
                          <path
                            d="M9 19c-5 1.5-5-2.5-7-3m14 6v-3.87a3.37 3.37 0 0 0-.94-2.61c3.14-.35 6.44-1.54 6.44-7A5.44 5.44 0 0 0 20 4.77 5.07 5.07 0 0 0 19.91 1S18.73.65 16 2.48a13.38 13.38 0 0 0-7 0C6.27.65 5.09 1 5.09 1A5.07 5.07 0 0 0 5 4.77a5.44 5.44 0 0 0-1.5 3.78c0 5.42 3.3 6.61 6.44 7A3.37 3.37 0 0 0 9 18.13V22">
                          </path>
                        </svg></a>
                      <a v-if="item.demo !== 'null'" :href="item.demo" target="_blank" rel="noreferrer"
                        title="View finished project" class="transition-all hover:text-accent">
                        <svg stroke="currentColor" fill="none" stroke-width="2" viewBox="0 0 24 24"
                          stroke-linecap="round" stroke-linejoin="round" height="18" width="18"
                          xmlns="http://www.w3.org/2000/svg">
                          <path d="M18 13v6a2 2 0 0 1-2 2H5a2 2 0 0 1-2-2V8a2 2 0 0 1 2-2h6"></path>
                          <polyline points="15 3 21 3 21 9"></polyline>
                          <line x1="10" y1="14" x2="21" y2="3"></line>
                        </svg></a>
                    </div>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </section>
    </article>
  </div>
</template>

<style>
.item-card:hover {
  transition: transform 0.3s ease;
  transform: translateY(-8px);
}

svg:hover {
  stroke: #87CEEB;
}

@keyframes fadeZoomIn {
  0% {
    opacity: 0;
    transform: scale(0.5);
  }

  100% {
    opacity: 1;
    transform: scale(1);
  }
}


/* Menggunakan animasi pada elemen yang diinginkan */
.fade-zoom-in {
  animation: fadeZoomIn 1s ease-in-out;
}

/* Gaya untuk tombol filter */
.filter-container {
  display: flex;
  gap: 10px;
  justify-content: center;
  margin-top: 20px;
}

.filter-btn {
  padding: 8px 16px; /* Padding untuk panjang border yang sama rata */
  border: 2px solid #87CEEB; /* Warna border biru langit */
  border-radius: 5px; /* Atur radius border sesuai kebutuhan */
  color: #fff; /* Warna teks putih */
  font-size: 14px; /* Ukuran font */
  cursor: pointer;
  transition: background-color 0.3s ease, color 0.3s ease, border-color 0.3s ease;
  box-sizing: border-box; /* Ukuran border sesuai padding */
 
}

.filter-btn:hover {
  background-color: #2c3e50; 
}

button:hover {
  transition: transform 0.3s ease;
  transform: translateY(-8px);
  stroke: #87CEEB;
}

@keyframes fadeZoomIn {
  0% {
    opacity: 0;
    transform: scale(0.5);
  }

  100% {
    opacity: 1;
    transform: scale(1);
  }
}
</style>