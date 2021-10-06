<template>
  <div class="container mx-auto mt-12 grid grid-cols-12 bg-blue-300">
    <!--個人資料 -->
    <div class="profile  col-span-3 bg-red-300 p-6 pb-10">
      <h2 class="font-bold text-3xl">個人資料 <strong class=" font-bold text-2xl">PROFILE</strong></h2>
       <img class="myself mx-auto rounded-full px-6 py-4" src="../assets/myself.jpg">
         <h1 class="text-5xl font-bold my-6">洪瑛蔚</h1>
      <ul>
        <li class="font-bold my-2">Mail: 4a33a006@stust.edu.tw</li>
        <li class="font-bold my-2">From: Taichung, Taiwan</li>
        <li class="font-bold my-2">
          Github:
          <a class="text-blue-500" href="https://github.com/because-hung"
            > https://github.com/because-hung</a
          >
        </li>
        <li class="font-bold my-2">Blog: <a class="text-blue-500" href="https://because-hung.medium.com/"> https://because-hung.medium.com/</a></li>
      </ul>
    </div>
      <!--技能 -->
      <div class="skillProject col-span-9 ">
      <h2 class="font-bold text-3xl my-4">技能 <strong class="text-red-500 font-bold text-2xl">SKILLS</strong></h2>
       <div class="skill py-6  grid  grid-rows-1 grid-cols-4">
      <div class="Css ">
         <h3 class="text-2xl font-bold mb-3 ">HTML / CSS </h3>
      <ul v-for="(item, i) in cssSkill" :key="i">
        <li class="text-xl my-1 ">{{ item }}</li>
      </ul>
      </div>
      <div class="Js border-l-4 ">
      <h3 class="text-2xl font-bold mb-3">JavaScript / Vue.js </h3>
      <ul v-for="(item, i) in jsSkill" :key="i">
        <li class="text-xl my-1 ">{{ item }}</li>
      </ul>
      </div>
      <div class="Other border-l-4 px-6">
        <h3 class="text-2xl font-bold mb-3">Other Skill </h3>
      <ul v-for="(item, i) in otherSkill" :key="i">
        <li class="text-xl my-1 ">{{ item }}</li>
      </ul>
      </div>
      <div class="Someskill border-l-4  px-6">
           <h3 class="text-2xl font-bold mb-3">略懂</h3>
      <ul v-for="(item, i) in knowSomeSkill" :key="i">
        <li class="text-xl my-1 ">{{ item }}</li>
      </ul>
      </div>
    </div>
      <!--作品 經歷 -->

    <div class="project font-bold text-3xl my-4">作品  <strong class="text-red-500 font-bold text-2xl">PROJECT</strong></div>
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
        'Sass / Scss',
        'RWD',
        'Flex / Grid'
      ],
      jsSkill: [
        'Nuxt',
        'Vue',
        'Vue Cli',
        'Vue Router',
        'JQuery',
        'ES5 / ES6',
        'promise / async.await'
      ],
      otherSkill: [
        'Webpack 5',
        'Git',
        'Zeplin'
      ],
      knowSomeSkill: [
        'Vuex',
        'React'
      ],
      project: [
        {
          title: '侑欣科技(接案)',
          info: '跟朋友合作的接案的作品，我負責的工作是服務內容、加工設備、合作客戶三個頁面的切版',
          skill: 'Nuxt / Tailwind.css / Grid.flex / RWD',
          url: '作品網址',
          img: '示意圖'
        },
        {
          title: 'Covid-19 疫情資訊整合頁',
          info: '作品的發想是想要做一些能對社會有幫助的網頁，後來發現政府疫情資訊網的資訊太多太繁雜，可能導致民眾不容易觀看，所以從中抓出幾個重點，整合出資訊明瞭的疫情整合資訊頁，使得民眾更方便閱讀資訊，更能了解疫情的狀況',
          skill: 'Nuxt / Tailwind.css / Grid.flex / Scss / RWD / axios / async.await / 第三方api',
          url: '作品網址',
          img: '示意圖'
        },
        {
          title: 'slack天然沐浴用品電商網站',
          info: '作品的發想是有想過往電商公司做發展，作品想模擬電商網站的架構跟邏輯，透過購物車和下訂單等功能能訓練js的實務應用，也能了解大概是怎麼運作的',
          skill: 'Vue / Bootstrap / flex / Scss / RWD / axios / promise / restful api',
          url: 'https://because-hung.github.io/vue.js-project-web/#/',
          img: '示意圖'
        },
        {
          title: '作品名稱',
          info: '敘述',
          skill: '使用的技術',
          url: '作品網址',
          img: '示意圖'
        }
      ]
    }
  }
}
</script>
