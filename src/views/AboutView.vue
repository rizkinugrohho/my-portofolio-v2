<script>
export default {
  data() {
    return {
      activeTab: 1,
      tech: [
        {
          id: 1,
          name: 'Kotlin',
          imageUrl: 'https://uxwing.com/wp-content/themes/uxwing/download/brands-and-social-media/kotlin-programming-language-icon.png',
          status: 'Advanced'
        },
        {
          id: 2,
          name: 'Flutter',
          imageUrl: 'https://uxwing.com/wp-content/themes/uxwing/download/brands-and-social-media/flutter-icon.png',
          status: 'Intermediate'
        },
        {
          id: 3,
          name: 'Javascript',
          imageUrl: 'https://cdn.icon-icons.com/icons2/2415/PNG/512/javascript_original_logo_icon_146455.png',
          status: 'Advance'
        },
        {
          id: 4,
          name: 'PHP',
          imageUrl: 'https://cdn.iconscout.com/icon/free/png-256/free-php-2038871-1720084.png',
          status: 'Advanced'
        },
        {
          id: 5,
          name: 'NodeJS',
          imageUrl: 'https://cdn.iconscout.com/icon/free/png-256/free-node-js-1174925.png',
          status: 'Advance'
        },
        {
          id: 6,
          name: 'VueJS',
          imageUrl: 'https://cdn.iconscout.com/icon/free/png-256/free-vue-282497.png?f=webp',
          status: 'Advance'
        },
        {
          id: 7,
          name: 'React Native',
          imageUrl: 'https://cdn4.iconfinder.com/data/icons/logos-3/600/React.js_logo-512.png',
          status: 'Beginner'
        },
        {
          id: 8,
          name: 'Codeigniter',
          imageUrl: 'https://cdn1.iconfinder.com/data/icons/logos-3/304/codeigniter-icon-512.png',
          status: 'Intermediate'
        },
        {
          id: 9,
          name: 'ReactJS',
          imageUrl: 'https://cdn4.iconfinder.com/data/icons/logos-3/600/React.js_logo-512.png',
          status: 'Intermediate'
        },
        {
          id: 10,
          name: 'Laravel',
          imageUrl: 'https://cdn.worldvectorlogo.com/logos/laravel-2.svg',
          status: 'Advance'
        },
        {
          id: 11,
          name: 'Java',
          imageUrl: 'https://cdn4.iconfinder.com/data/icons/logos-and-brands/512/181_Java_logo_logos-256.png',
          status: 'Intermediate'
        },
        {
          id: 12,
          name: 'Tailwind',
          imageUrl: 'https://upload.wikimedia.org/wikipedia/commons/d/d5/Tailwind_CSS_Logo.svg',
          status: 'Intermediate'
        }
      ],
      tools: [
        {
          id: 1,
          name: 'Android Studio',
          imageUrl: 'https://uxwing.com/wp-content/themes/uxwing/download/brands-and-social-media/android-studio-icon.png',
          status: 'Android Tools'
        },
        {
          id: 2,
          name: 'Git',
          imageUrl: 'https://git-scm.com/images/logos/downloads/Git-Icon-1788C.png',
          status: 'Version Control'
        },
        {
          id: 3,
          name: 'GitHub',
          imageUrl: 'https://seeklogo.com/images/G/github-logo-2E3852456C-seeklogo.com.png',
          status: 'Git Hosting'
        },
        {
          id: 4,
          name: 'NPM',
          imageUrl: 'https://cdn.iconscout.com/icon/free/png-256/free-npm-3-1175132.png',
          status: 'Package Manager'
        },
        {
          id: 5,
          name: 'MySQL',
          imageUrl: 'https://cdn-icons-png.flaticon.com/512/5968/5968313.png',
          status: 'Database'
        },
        {
          id: 6,
          name: 'MongoDB',
          imageUrl: 'https://uxwing.com/wp-content/themes/uxwing/download/brands-and-social-media/mongodb-icon.png',
          status: 'Mongoose Database'
        },
        {
          id: 7,
          name: 'Visual Studio',
          imageUrl: 'https://uxwing.com/wp-content/themes/uxwing/download/brands-and-social-media/visual-studio-code-icon.png',
          status: 'Tools'
        },
      ]
    };
  },
  methods: {
    downloadResume() {
      window.open('https://drive.google.com/file/d/1xpxskcdqM6JSIXW63ZWwpa9dxD0pjOZq/view?usp=sharing', '_blank');
    },
    whatsApp() {
      window.open('https://api.whatsapp.com/send/?phone=6281586261383&text=Hello%20Rizki%20Nugroho,%20nice%20to%20meet%20you!', '_blank');
    },
    email() {
      window.open('mailto:rizkynhg@gmail.com?subject=Hello,%20I%20have%20a%20job%20for%20you.', '_blank');
    },
  }
}
</script>
<template>
  <div
    class="bg-[#1e1e1f] px-5 py-5 md:px-12 md:py-10 text-left border border-[#383838] rounded-3xl text-sky-50 mx-3 mb-5">
    <article data-page="about">

      <header>
        <div class="text-2xl font-bold text-white mb-5 fadein-bot title-section flex items-center">
          About Me &nbsp;
          <div class="h-[1px] w-32 bg-sky-200 md:w-96 aos-init aos-animate" data-aos="zoom-in-left"
            data-aos-duration="600"></div>
        </div>
      </header>

      <section
        class="text-sm md:text-lg text-justify flex flex-col gap-4 md:flex-row md:gap-8 md:justify-left md:items-center">
        <div class="flex justify-center">
          <img class="w-9/12 rounded-full mb-3 fadein-up" src="/img/profil2.png" alt="Foto">
        </div>
        <div class="md:w-7/12">
          <p class="text-base mb-3 md:mb-7 fadein-left fadeins-1">
            &nbsp; &nbsp; &nbsp; Hi everyone! My name is Rizki Nugroho.
            I am an 25 year old living in Tangerang, indonesia.
            I have over a year of experience in Back-end web Development and Android Development.
            Mastered various programming languages and frameworks.
          </p>
          <p class="text-base mb-3 fadein-left fadeins-2">
            &nbsp; &nbsp; &nbsp; My job is to build your website or applications to be functional and user-friendly yet
            still attractive.
            In addition, I provide a personal touch to your product and ensure that the website catches attention and is
            easy to use.
            My goal is to convey your message and identity in the most creative way. If you are interested in hiring me,
            please contact the listed contact.
          </p>
          <div class="py-3 flex">
            <!-- Tombol pertama 
            <button
        class="fadein-bot fade-500 flex items-center py-2 px-4 text-sm font-medium rounded-lg border transition duration-300 md:py-2.5 md:px-5 text-sky-200 border-sky-200 hover:bg-sky-200 hover:bg-opacity-10 bg-transparent focus:outline-none"
        @click="downloadResume"><svg
          xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" fill="currentColor" class="mr-2 w-4 h-4">
          <path fill-rule="evenodd"
            d="M5.625 1.5H9a3.75 3.75 0 013.75 3.75v1.875c0 1.036.84 1.875 1.875 1.875H16.5a3.75 3.75 0 013.75 3.75v7.875c0 1.035-.84 1.875-1.875 1.875H5.625a1.875 1.875 0 01-1.875-1.875V3.375c0-1.036.84-1.875 1.875-1.875zm5.845 17.03a.75.75 0 001.06 0l3-3a.75.75 0 10-1.06-1.06l-1.72 1.72V12a.75.75 0 00-1.5 0v4.19l-1.72-1.72a.75.75 0 00-1.06 1.06l3 3z"
            clip-rule="evenodd"></path>
          <path
            d="M14.25 5.25a5.23 5.23 0 00-1.279-3.434 9.768 9.768 0 016.963 6.963A5.23 5.23 0 0016.5 7.5h-1.875a.375.375 0 01-.375-.375V5.25z">
          </path>
        </svg>Download Resume</button> -->
            <!-- Tombol Kedua -->
            <button
              class="fadein-bot fade-500 flex items-center py-2 px-4 text-sm font-medium rounded-lg border transition duration-300 md:py-2.5 md:px-5 text-sky-200 border-sky-200 hover:bg-sky-200 hover:bg-opacity-10 bg-transparent focus:outline-none ml-2"
              @click="whatsApp"><svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" fill="currentColor"
                class="mr-2 w-4 h-4">
                <path fill-rule="evenodd"
                  d="M5.625 1.5H9a3.75 3.75 0 013.75 3.75v1.875c0 1.036.84 1.875 1.875 1.875H16.5a3.75 3.75 0 013.75 3.75v7.875c0 1.035-.84 1.875-1.875 1.875H5.625a1.875 1.875 0 01-1.875-1.875V3.375c0-1.036.84-1.875 1.875-1.875zm5.845 17.03a.75.75 0 001.06 0l3-3a.75.75 0 10-1.06-1.06l-1.72 1.72V12a.75.75 0 00-1.5 0v4.19l-1.72-1.72a.75.75 0 00-1.06 1.06l3 3z"
                  clip-rule="evenodd"></path>
                <path
                  d="M14.25 5.25a5.23 5.23 0 00-1.279-3.434 9.768 9.768 0 016.963 6.963A5.23 5.23 0 0016.5 7.5h-1.875a.375.375 0 01-.375-.375V5.25z">
                </path>
              </svg>WhatsApp</button>

            <!-- Tombol Ketiga -->
            <button
              class="fadein-bot fade-500 flex items-center py-2 px-4 text-sm font-medium rounded-lg border transition duration-300 md:py-2.5 md:px-5 text-sky-200 border-sky-200 hover:bg-sky-200 hover:bg-opacity-10 bg-transparent focus:outline-none ml-2"
              @click="email"><svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" fill="currentColor"
                class="mr-2 w-4 h-4">
                <path fill-rule="evenodd"
                  d="M5.625 1.5H9a3.75 3.75 0 013.75 3.75v1.875c0 1.036.84 1.875 1.875 1.875H16.5a3.75 3.75 0 013.75 3.75v7.875c0 1.035-.84 1.875-1.875 1.875H5.625a1.875 1.875 0 01-1.875-1.875V3.375c0-1.036.84-1.875 1.875-1.875zm5.845 17.03a.75.75 0 001.06 0l3-3a.75.75 0 10-1.06-1.06l-1.72 1.72V12a.75.75 0 00-1.5 0v4.19l-1.72-1.72a.75.75 0 00-1.06 1.06l3 3z"
                  clip-rule="evenodd"></path>
                <path
                  d="M14.25 5.25a5.23 5.23 0 00-1.279-3.434 9.768 9.768 0 016.963 6.963A5.23 5.23 0 0016.5 7.5h-1.875a.375.375 0 01-.375-.375V5.25z">
                </path>
              </svg>Email</button>
          </div>
        </div>

      </section>
      <div class="text-2xl font-bold text-white mb-5 fadein-bot title-section flex items-center">
        Experiences &nbsp;
      </div>
      <section class="container experiences">
        <div class="flex items-center gap-4"> <!-- Flex container untuk gambar dan teks -->
          <div class="item-tech flex gap-2 px-2 py-2 hover hover:bg-opacity-10 md:gap-3 lg:px-3">
            <div class="flex h-12 w-12 p-0 lg:h-16 lg:w-16 lg:p-2 zoom-in">
              <img alt="HTML" loading="lazy" width="32" height="32" decoding="async"
                class="img-tech drop-shadow-xl transition-all duration-300 h-[65%] w-[65%] lg:h-[85%] lg:w-[85%]"
                src="https://media.licdn.com/dms/image/C4D0BAQFyp5sVKNaskw/company-logo_200_200/0/1631333075043?e=2147483647&v=beta&t=4vCHg_BToWKJyyeVi8wpiEziHPLf3qycPhp7n8zAll4"
                style="color: transparent;">
            </div>
            <div class="text-base mb-3 fadein-left"> <!-- Container untuk teks -->
              <p class="text-xl text-sky-200 font-bold">Web Developer</p>
              <p class="text-base text-sky-200">PT Dutaflow Hidrolik · Full time</p>
              <p class="text-base text-sky-100">Nov 2021 - Present</p>
              <ul class="text-base">
                <li>- Developing Company Profile using PHP Laravel Frameworks and Vue js</li>
                <li>- Maintenance and fix some bugs.</li>
                <li>- Writing clean, functional code on the front- and back-end.</li>
              </ul>
            </div>
          </div>
        </div>
        <div class="h-[1px] w-32 bg-sky-200 md:w-98 aos-init aos-animate" data-aos="zoom-in-left"
          data-aos-duration="600"></div><br>

        <div class="flex items-center gap-4"> <!-- Flex container untuk gambar dan teks -->
          <div class="item-tech flex gap-2 px-2 py-2 hover hover:bg-opacity-10 md:gap-3 lg:px-3">
            <div class="flex h-12 w-12 p-0 lg:h-16 lg:w-16 lg:p-2 zoom-in">
              <img alt="HTML" loading="lazy" width="32" height="32" decoding="async"
                class="img-tech drop-shadow-xl transition-all duration-300 h-[65%] w-[65%] lg:h-[85%] lg:w-[85%]"
                src="https://play-lh.googleusercontent.com/p5E-YoYPD-PUZQw9zb9z4si0JRhkpuivjnEaGYTSoPyv6WyQ4IgVrmARsjXN38KM0Q"
                style="color: transparent;">
            </div>
            <div class="text-base mb-3 fadein-left"> <!-- Container untuk teks -->
              <p class="text-xl text-sky-200 font-bold">Mobile React Developer</p>
              <p class="text-base text-sky-200">Kominfo Digitalent · Internship</p>
              <p class="text-base text-sky-100">May 2024 - Jul 2024</p>
              <ul class="text-base">
                <li>This program includes completing various tasks related to Mobile Apps Development With React, such
                  as:
                </li>
                <li>- Javascript: Basic Intermediate and Expert.</li>
                <li>- React: Core Components of React.</li>
                <li>- React Native and APIs.</li>
                <li>- Navigation from React Native.</li>
                <li>- Git: Git Principles, Operations, and Git Features.</li>
                <li>- API: React Native and API.</li>
              </ul>
            </div>
          </div>
        </div>
        <div class="h-[1px] w-32 bg-sky-200 md:w-98 aos-init aos-animate" data-aos="zoom-in-left"
          data-aos-duration="600"></div><br>

          <div class="flex items-center gap-4"> <!-- Flex container untuk gambar dan teks -->
          <div class="item-tech flex gap-2 px-2 py-2 hover hover:bg-opacity-10 md:gap-3 lg:px-3">
            <div class="flex h-12 w-12 p-0 lg:h-16 lg:w-16 lg:p-2 zoom-in">
              <img alt="HTML" loading="lazy" width="32" height="32" decoding="async"
                class="img-tech drop-shadow-xl transition-all duration-300 h-[65%] w-[65%] lg:h-[85%] lg:w-[85%]"
                src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcRKffCM7Op1KQ8VcDv1EokYhSTywz13VG8Wmw&s"
                style="color: transparent;">
            </div>
            <div class="text-base mb-3 fadein-left"> <!-- Container untuk teks -->
              <p class="text-xl text-sky-200 font-bold">Mobile Apps Developer</p>
              <p class="text-base text-sky-200">Bank Mandiri x Rakamin Academy · Internship</p>
              <p class="text-base text-sky-100">Sep 2023 - oct 2023</p>
              <ul class="text-base">
                <li>The program involves completing various tasks related to Mobile Apps Development for Bank Mandiri, such
              as:</li>
            <li>- Android: Environment & Lifecycle, UI and Design Pattern, RecyclerView, and Database.</li>
            <li>- Kotlin: XML, Gradle, Principles of Kotlin, and OOP.</li>
            <li>- iOS: Swift, XCode Mastery, UI in iOS, Collections and Localization, and Data Persistence and Web
              Services.</li>
            <li>- Unit Testing: Principles of Unit Testing, Unit Testing Tools, Unit Testing Instrument.</li>
            <li>- Gitlab: Principles of Gitlab, Operation, and Features of Gitlab.</li>
            <li>- API (Aplication Programing Interface): Principles of API, Basic Operation of API, Restful API.</li>
          </ul>
            </div>
          </div>
        </div>
        <div class="h-[1px] w-32 bg-sky-200 md:w-98 aos-init aos-animate" data-aos="zoom-in-left"
          data-aos-duration="600"></div><br>

          <div class="flex items-center gap-4"> <!-- Flex container untuk gambar dan teks -->
          <div class="item-tech flex gap-2 px-2 py-2 hover hover:bg-opacity-10 md:gap-3 lg:px-3">
            <div class="flex h-12 w-12 p-0 lg:h-16 lg:w-16 lg:p-2 zoom-in">
              <img alt="HTML" loading="lazy" width="32" height="32" decoding="async"
                class="img-tech drop-shadow-xl transition-all duration-300 h-[65%] w-[65%] lg:h-[85%] lg:w-[85%]"
                src="https://pangrampangram.com/cdn/shop/articles/442269ac56eddaecd3fa3dd752c38870_1920x.jpg?v=1631828825"
                style="color: transparent;">
            </div>
            <div class="text-base mb-3 fadein-left"> <!-- Container untuk teks -->
              <p class="text-xl text-sky-200 font-bold">Web Developer</p>
              <p class="text-base text-sky-200">Upwork · Freelancer</p>
              <p class="text-base text-sky-100">Apr 2022 - Jun 2023</p>
              <ul class="text-base">
                <li>- Engineered modern applications with Node Js, React JS</li>
            <li>- Work on application deployment to cloud servers.</li>
            <li>- Confirmed that completed software met client requirements.</li>
            <li>- Bug Fixing.</li>
          </ul>
            </div>
          </div>
        </div>
      </section>

    </article>
  </div>

  <div class="px-5 py-5 md:px-12 md:py-10 text-left text-sky-50 mx-3">
    <article data-page="about">
      <header>
        <div class="text-2xl font-bold text-white mb-5 fadein-bot title-section flex items-center">
          <div class="h-[1px] w-10 bg-sky-200 md:w-20 aos-init aos-animate" data-aos="zoom-in-left"
            data-aos-duration="600"></div>
          &nbsp; Skills
        </div>
      </header>
      <section>
        <div>
          <ul class="flex flex-wrap text-sm font-medium text-center text-gray-500 dark:text-gray-400 mb-5">
            <li class="mr-2">
              <button class="inline-block px-4 py-3 rounded-lg hover:text-white"
                :class="{ 'text-sky-200 bg-sky-200 bg-opacity-10': activeTab === 1 }" @click="activeTab = 1">Tech
                Stack</button>
            </li>
            <li class="mr-2">
              <button class="inline-block px-4 py-3 rounded-lg hover:text-white"
                :class="{ 'text-sky-200 bg-sky-200 bg-opacity-10': activeTab === 2 }"
                @click="activeTab = 2">Tools</button>
            </li>
          </ul>
        </div>
        <div v-show="activeTab === 1">
          <div class="grid grid-cols-2 gap-4 pb-32 md:grid-cols-3 md:gap-8 xl:grid-cols-4 xl:gap-10 2xl:gap-12">
            <div v-for="item in tech" :key="item.id">
              <div
                class="item-tech flex cursor-pointer items-center gap-2 rounded border border-sky-200 px-2 py-2 hover:bg-sky-200 hover:bg-opacity-10 md:gap-3 lg:px-3">
                <div class="flex h-12 w-12 items-center justify-center p-0 lg:h-16 lg:w-16 lg:p-2 zoom-in">
                  <img alt="HTML" loading="lazy" width="32" height="32" decoding="async" data-nimg="1"
                    class="img-tech drop-shadow-xl transition-all duration-300 h-[65%] w-[65%] lg:h-[85%] lg:w-[85%]  "
                    :src="item.imageUrl" style="color: transparent;">
                </div>
                <div class="flex items-center text-sm md:text-base lg:text-lg">
                  <div class="tech font-medium text-secondary transition-all duration-300 translate-y-0 ">{{ item.name
                    }}
                  </div>
                  <div
                    class="status-tech opacity-0 absolute mt-5 text-[10px] text-sky-200 transition-all duration-300 md:text-xs lg:text-sm">
                    {{ item.status }}</div>
                </div>
              </div>
            </div>
          </div>
        </div>
        <div v-show="activeTab === 2">
          <div class="grid grid-cols-2 gap-4 pb-32 md:grid-cols-3 md:gap-8 xl:grid-cols-4 xl:gap-10 2xl:gap-12">
            <div v-for="item in tools" :key="item.id">
              <div
                class="item-tech flex cursor-pointer items-center gap-2 rounded border border-sky-200 px-2 py-2 hover:bg-sky-200 hover:bg-opacity-10 md:gap-3 lg:px-3">
                <div class="flex h-12 w-12 items-center justify-center p-0 lg:h-16 lg:w-16 lg:p-2 zoom-in">
                  <img alt="HTML" loading="lazy" width="32" height="32" decoding="async" data-nimg="1"
                    class="img-tech drop-shadow-xl transition-all duration-300 h-[65%] w-[65%] lg:h-[85%] lg:w-[85%]  "
                    :src="item.imageUrl" style="color: transparent;">
                </div>
                <div class="flex items-center text-sm md:text-base lg:text-lg">
                  <div class="tech font-medium text-secondary transition-all duration-300 translate-y-0 ">{{ item.name
                    }}
                  </div>
                  <div
                    class="status-tech opacity-0 absolute mt-5 text-[10px] text-sky-200 transition-all duration-300 md:text-xs lg:text-sm">
                    {{ item.status }}</div>
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
.fadein-left {
  opacity: 0;
  animation: fadeInLeft 0.5s ease-out forwards;
}

@keyframes fadeInLeft {
  0% {
    opacity: 0;
    transform: translateX(100%);
  }

  100% {
    opacity: 1;
    transform: translateX(0);
  }
}

.fadeins-1 {
  animation-delay: 500ms;
}

.fadeins-2 {
  animation-delay: 800ms;
}

.img-tech,
.tech {
  transition: transform 0.3s ease;
}

.item-tech:hover .img-tech {
  transform: scale(1.3);
}

.item-tech:hover .tech {
  transform: translateY(-12px);
}

.item-tech:hover .status-tech {
  opacity: 1;
}

.experiences {
  padding: 5px;
  margin: 5px;
  border-radius: 10px;
}

.experience-item {
  padding: 10px;
  border-left: 1px solid rgba(135, 206, 235, .5)
}
</style>
