<template>
  <div class="container mx-auto mt-12 xl:grid xl:grid-cols-12">
    <!--個人資料 -->
    <div class="profileSkill col-span-5 px-6 ">
    <div class="profile  text-black bg-blue-500 rounded-2xl p-4 sm:flex justify-center ">
      <div class="imgInfo">
        <h2 class="font-bold text-3xl">
          個人資料 <strong class=" font-bold text-2xl">PROFILE</strong>
        </h2>
        <img
          class="myself mx-auto rounded-full px-6 py-4 w-72 h-56 "
          src="../assets/myself.jpg"
        />
        <h1 class="text-5xl font-bold my-6">洪瑛蔚</h1>
      </div>
      <ul class="contact pb-4 sm:py-12 sm:ml-8">
        <li class="font-bold  my-2 sm:my-8 text-base">Mail: barryhung841212@gmail.com</li>
        <li class="font-bold  my-2 sm:my-8 text-base">From: Taichung, Taiwan</li>
        <li class="font-bold  my-2 sm:my-8">
          Github:
           <br>
          <a class=" text-base bg-yellow-400 sm:bg-transparent p-1 text-blue-500" href="https://github.com/because-hung">
            https://github.com/because-hung</a
          >
        </li>
        <li class="font-bold my-2 sm:my-8 ">
          Blog:
          <br>
          <a class="text-base breakWord bg-yellow-400 sm:bg-transparent p-1 text-blue-500" href="https://because-hung.medium.com/">
            https://because-hung.medium.com/</a
          >
        </li>
      </ul>
    </div>
    <!--技能 -->
    <div class="skillProject">
      <h2 class="font-bold text-3xl mt-10 ">
        <span class="text-4xl md:text-5xl bg-red-500 text-white p-2 mr-2 ">技能</span>
        <strong class="text-red-500 font-bold text-2xl" >SKILLS</strong>
      </h2>
      <div class="skill py-6 sm:px-6 lg:px-0 grid  grid-rows-1 grid-cols-1 sm:grid-cols-2 gap-x-5 gap-y-12">
        <div class="Css blur-sm border-b-4 border-r-4 border-gray-800 rounded-2xl   shadow-xl  p-2 ">
          <h3 class="text-2xl font-bold mb-3 lg:text-yellow-200">HTML / CSS</h3>
          <ul class="flex flex-wrap justify-center xl:justify-start">
            <li
              v-for="(item, i) in cssSkill"
              :key="i"
              class="font-bold m-2 bg-green-300 w-28 rounded-full p-2 flex items-center justify-center"
            >
              {{ item }}
            </li>
          </ul>
        </div>
        <div class="Js blur-sm  border-b-4 border-r-4 border-gray-800 rounded-2xl shadow-xl   p-2">
          <h3 class="text-2xl font-bold mb-3 lg:text-yellow-200">JavaScript / Vue.js</h3>
          <ul class="flex flex-wrap justify-center xl:justify-start">
            <li
              v-for="(item, i) in jsSkill"
              :key="i"
              class="font-bold m-2 bg-green-300 w-28 rounded-full p-2 flex items-center justify-center"
            >
              {{ item }}
            </li>
          </ul>
        </div>
        <div class="Other blur-sm border-b-4 border-r-4 border-gray-800 rounded-2xl  shadow-xl  p-2">
          <h3 class="text-2xl font-bold mb-3 lg:text-yellow-200">Other Skill</h3>
          <ul class="flex flex-wrap justify-center xl:justify-start">
            <li
              v-for="(item, i) in otherSkill"
              :key="i"
              class="font-bold m-2 bg-green-300 w-28 rounded-full p-2 flex items-center justify-center"
            >
              {{ item }}
            </li>
          </ul>
        </div>
      </div>
      <!--作品 經歷 -->
    </div>
    </div>
    <div class="projectInfo col-span-7 sm:ml-6 mb-10">
    <div class="project font-bold text-xl mt-6 ">
      <div class="projectTitle mb-8">
        <span class="text-4xl md:text-5xl bg-red-500 text-white p-2 mr-2 ">經歷 / 作品 </span>
        <strong class="text-red-500 font-bold text-2xl ">PROJECT</strong>
        </div>
        <div class="projectCard px-8 sm:px-12 font-medium text-left ">
          <ul
            class=" flex flex-col  py-8 blur ring ring-offset-4 ring-gray-600 text-white p-6 rounded-2xl"
            v-for="(item, i) in experience"
            :key="i"
          >
            <li class="mt-4 mb-6">
               <span class="bg-purple-600 p-2 px-4 text-white font-bold ">{{ item.categories }}</span>
            </li>
              <li class="mb-2">
              <span class="bg-blue-600 p-2 px-4 text-white font-bold">{{ item.company }}</span>
            </li>
            <li class="my-2">
              主要技術:
              <p class=" leading-normal font-bold text-base">{{
                item.skill
              }}</p>
            </li>
            <li class="my-2">
              技術做的事:
              <p class=" leading-normal font-bold text-base">{{
                item.skillDo
              }}</p>
            </li>
            <li class="my-2">
            敘述:
              <p class="info leading-normal mt-4  font-bold  text-base">
                {{ item.info }}
              </p>
            </li>
            <li v-if="item.url" class="my-6 flex flex-col "><span>網址</span><a class="mt-2 pl-2  p-1 bg-yellow-300 text-blue-600 breakWord  text-base" :href="item.url"> {{item.url}}</a></li>
          </ul>
          <ul
            class=" flex flex-col  py-8 blur ring ring-offset-4 ring-gray-600 text-white p-6 rounded-2xl"
            v-for="(item, i) in project"
            :key="i"
          >
            <li class="mt-4 mb-6">
               <span class="bg-purple-600 p-2 px-4 text-white font-bold ">{{ item.categories }}</span>
            </li>
              <li class="mb-2">
              <span class="bg-blue-600 p-2 px-4 text-white font-bold">{{ item.title }}</span>
            </li>
            <li class="my-2">
              主要技術:
              <p class=" leading-normal font-bold text-base">{{
                item.skill
              }}</p>
            </li>
            <li class="my-2">
              技術做的事:
              <p class=" leading-normal font-bold text-base">{{
                item.skillDo
              }}</p>
            </li>
            <li class="my-2">
            敘述:
              <p class="info leading-normal mt-4  font-bold  text-base">
                {{ item.info }}
              </p>
            </li>
            <li class="my-6 flex flex-col "><span>作品網址</span><a class="mt-2 pl-2  p-1 bg-yellow-300 text-blue-600 breakWord  text-base" :href="item.url"> {{item.url}}</a></li>
            <li class="my-1 flex flex-col "><span>Github</span> <a class="mt-2 pl-2  p-1 bg-yellow-300 text-blue-600 breakWord  text-base" :href="item.github"> {{item.github}}</a></li>
          </ul>
        </div>
      </div>
      </div>
  </div>
</template>

<script>
export default {
  data () {
    return {
      cssSkill: [
        'Tailwind.css',
        'Bootstrap',
        'Element UI / Plus',
        'Pug',
        'Sass / Scss',
        'RWD'
      ],
      jsSkill: [
        'Nuxt',
        'Vue 2 / 3',
        'Vuex',
        'JQuery',
        'ES5 / ES6',
        'Promise / Async.Await'
      ],
      otherSkill: ['Webpack 5', 'Git', 'Zeplin'],
      experience: [
        {
          categories: '經歷',
          company: '泉耀國際 (2022/6 - 2022/10)',
          info:
            '串接並整合 Api 資料，顯示在畫面上，依照業務需求做出所需功能，依照設計稿切出所需的樣式，功能有後台報表頁面，信箱頁面，還有一些跳轉 skype、複製文字等等功能，維護專案修復 bug 和頁面樣式的換皮及重構切版',
          skill:
            'Vue 2 / Vue 3 / Css / Sass / Pug / Element Plus / AngularJS',
          skillDo:
            '使用 Vue 2 / 3 開發功能及維護專案，串接並整合 Api 資料，樣式使用 Css 開發及調整版面，偶爾搭配 Element UI 及 Plus 做使用，後台專案使用 AngularJS 維護及開發',
          url: ''
        },
        {
          categories: '經歷',
          company: '新穎資訊 (2022/2 - 2022/4)',
          info:
            '串接並整合 Api 資料，顯示在畫面上，依照業務需求做出篩選功能(篩選特定條件)，釘選功能(釘選想關注的資訊)，收藏功能(把想要的資訊放入我的最愛)，倒數功能(倒數完改變資料狀態)，Code Review 同事程式碼，維護專案',
          skill:
            'Vue 3 / Vuex / Bootstrap 5 ',
          skillDo:
            '使用 Vue 3 開發功能及維護專案，串接並整合 Api 資料，Bootstrap 5 調整專案版面樣式，專案切版不是我負責，Vuex 建立資源共享與管理',
          url: ''
        },
        {
          categories: '經歷',
          company: '侑欣科技 (接案)',
          info:
            '與朋友合作的接案，使用 Zeplin 看設計稿，依照設計稿切出所需的樣式，負責服務內容，加工設備，合作客戶三個頁面的切版',
          skill:
            'Nuxt / Tailwind.css / Grid',
          skillDo:
            '使用 Tailwind.css 做快速開發，Grid 做版面切版',
          url: 'https://www.yooxin-tech.com/'
        }
      ],
      project: [
        {
          categories: '作品',
          title: 'Covid-19 疫情資訊整合頁',
          info:
            '作品的特色是仿 google 網頁的介面樣式，在網路上還沒看過類似的作品，是一個滿新穎又獨一無二的作品，作品的發想是想要做一些能對社會有幫助的網頁，後來發現政府疫情資訊網的資訊太多太繁雜，可能導致民眾不容易觀看，所以從中抓出幾個重點，整合出資訊明瞭的疫情整合資訊頁，使得民眾更方便閱讀資訊，更能了解疫情跟疫苗的狀況，另一方面是想整合新學到的技術(Nuxt、Tailwind、Async.Await、Grid)，做出新的作品',
          skill:
            'Nuxt / Tailwind.css / Async.Await / 第三方 Api / 部屬 Heroku',
          skillDo:
            '把政府複雜的圖表資訊，抓出其中重點，整理出一個簡單易懂資訊頁面，串接並整合政府 Api 資料，呈現於畫面，把新學到的技術 Nuxt、Tailwind、Async.Await、Grid 使用在作品上',
          url: 'https://info-covid19-project.herokuapp.com/',
          github: 'https://github.com/because-hung/Covid-19-Project'
        },
        {
          categories: '作品',
          title: 'slack 天然沐浴用品電商網站',
          info:
            '作品的發想是有想過往電商公司做發展，作品想模擬電商網站的架構跟邏輯，透過購物車和下訂單等功能能訓練 Js 的實務邏輯應用，也能了解到串接 Api 的運作，這是我的第一個作品，在這其中學到了 Js 實務應用、Api 邏輯、切版實務、如何使用套件等等',
          skill:
            'Vue 2 / Bootstrap 4 / Sass / Promise / Restful Api',
          skillDo:
            '這個作品首頁運用 AOS 套件做動畫還有 Swiper 輪播，呈現網頁動態效果，讓版面活潑生動一些，運用 Bootstrap 4 快速切出商品頁面，運用 Vue 2 串接 Api 經過資料處理後顯示在畫面上，做出購物車與下訂單的功能模擬購物的行為，也建立後台產品新增刪除訂單管理功能',
          url: 'https://because-hung.github.io/vue.js-project-web/#/',
          github: 'https://github.com/because-hung/vue.js-project-web'
        },
        {
          categories: '作品',
          title: '仿 Youtube 靜態網頁',
          info: '看了一些自學的文章，上面說進步的方式，是可以找一些主流的頁面模仿切版，所以找了 Youtube 當模板，模仿其介面樣式去練習切版，並嘗試以 Github Pages 以外的方法去部屬，最後選擇了 heroku',
          skill: 'Nuxt / Css / Sass / 部屬 Heroku ',
          skillDo: '這個作品比較特別，給自己的練習跟挑戰，沒使用任何 Css 框架，只使用原生 Css 搭配 Sass 去切出類似 Youtube 的樣式，此作品沒任何功能，只是一個靜態頁面去做切版',
          url: 'https://ui-youtube.herokuapp.com/',
          github: 'https://github.com/because-hung/Youtube-Project'
        }
      ]
    }
  }
}
</script>
<style lang="scss">
body{
    background-image: url(../assets/pcBg.jpg);
      background-size: cover;
  background-position: center center;
}
@media (max-width:768px) {
  body{
    background-image: url(../assets/mobileBg.jpg);
      background-size: cover;
  background-position: left center;
}
}
.profile {
  background-image: url(../assets/profileBg.jpg);
  background-size: cover;
  background-position: center center;
}
.blur-sm{
  backdrop-filter: blur(12px);
}
.blur{
  backdrop-filter: blur(20px);
}
.breakWord{
 word-break: break-all;
}
</style>
