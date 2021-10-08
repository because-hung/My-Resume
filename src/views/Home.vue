<template>
  <div class="container mx-auto mt-12 grid grid-cols-12">
    <!--個人資料 -->
    <div class="profileSkill col-span-5">
    <div class="profile  text-black bg-blue-500 p-4 flex justify-center ">
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
      <ul class="py-12 ml-8">
        <li class="font-bold my-8">Mail: 4a33a006@stust.edu.tw</li>
        <li class="font-bold my-8">From: Taichung, Taiwan</li>
        <li class="font-bold my-8">
          Github:
          <a class="text-blue-500" href="https://github.com/because-hung">
            https://github.com/because-hung</a
          >
        </li>
        <li class="font-bold my-2">
          Blog:
          <a class="text-blue-500" href="https://because-hung.medium.com/">
            https://because-hung.medium.com/</a
          >
        </li>
      </ul>
    </div>
    <!--技能 -->
    <div class="skillProject ml-10 ">
      <h2 class="font-bold text-3xl mt-6 ">
        <span class="text-5xl bg-red-500 text-white p-2 mr-2">技能</span>
        <strong class="text-red-500 font-bold text-2xl" >SKILLS</strong>
      </h2>
      <div class="skill py-6  grid  grid-rows-1 grid-cols-2 gap-x-5 gap-y-12">
        <div class="Css blur   shadow-xl  p-2 ">
          <h3 class="text-2xl font-bold mb-3 ">HTML / CSS</h3>
          <ul class="flex flex-wrap ">
            <li
              v-for="(item, i) in cssSkill"
              :key="i"
              class="font-bold m-2 bg-green-300 w-28 rounded-full p-2"
            >
              {{ item }}
            </li>
          </ul>
        </div>
        <div class="Js blur shadow-xl   p-2">
          <h3 class="text-2xl font-bold mb-3">JavaScript / Vue.js</h3>
          <ul class="flex flex-wrap ml-4">
            <li
              v-for="(item, i) in jsSkill"
              :key="i"
              class="font-bold m-2 bg-green-300 w-28 rounded-full p-2"
            >
              {{ item }}
            </li>
          </ul>
        </div>
        <div class="Other blur  shadow-xl  p-2">
          <h3 class="text-2xl font-bold mb-3">Other Skill</h3>
          <ul class="flex flex-wrap">
            <li
              v-for="(item, i) in otherSkill"
              :key="i"
              class="font-bold m-2 bg-green-300 w-28 rounded-full p-2"
            >
              {{ item }}
            </li>
          </ul>
        </div>
        <div class="Someskill blur  shadow-xl  p-2">
          <h3 class="text-2xl font-bold mb-3">略懂</h3>
          <ul class="flex flex-wrap">
            <li
              v-for="(item, i) in knowSomeSkill"
              :key="i"
              class="font-bold m-2 bg-green-300 w-28 rounded-full p-2"
            >
              {{ item }}
            </li>
          </ul>
        </div>
      </div>
      <!--作品 經歷 -->
    </div>
    </div>
    <div class="projectInfo col-span-7 ml-6">
    <div class="project font-bold text-xl mt-6 ">
        <span class="text-5xl bg-red-500 text-white p-2 mr-2 ">作品 </span>
        <strong class="text-red-500 font-bold text-2xl">PROJECT</strong>
        <div class="projectCard px-12 font-medium text-left ">
          <ul
            class=" flex flex-col my-6 bg-white p-6"
            v-for="(item, i) in project"
            :key="i"
          >
            <li class="mt-8 mb-2 ">
              作品: <span class="bg-blue-700 p-2 text-white font-bold ">{{ item.title }}</span>
            </li>
            <li class="my-2 ">
              技術:
              <span class=" leading-normal font-bold">{{
                item.skill
              }}</span>
            </li>
            <li class="my-2 ">
            敘述:
              <p class="info leading-normal mt-4  font-bold ">
                {{ item.info }}
              </p>
            </li>
            <li class="my-6">作品網址 <span></span></li>
            <li class="my-6">示意圖 <span></span></li>
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
      otherSkill: ['Webpack 5', 'Git', 'Zeplin'],
      knowSomeSkill: ['Vuex', 'React'],
      project: [
        {
          title: 'Covid-19 疫情資訊整合頁',
          info:
            '作品的發想是想要做一些能對社會有幫助的網頁，後來發現政府疫情資訊網的資訊太多太繁雜，可能導致民眾不容易觀看，所以從中抓出幾個重點，整合出資訊明瞭的疫情整合資訊頁，使得民眾更方便閱讀資訊，更能了解疫情的狀況',
          skill:
            'Nuxt / Tailwind.css / Grid.flex / Scss / RWD / axios / async.await / 第三方api',
          url: '作品網址',
          img: '示意圖'
        },
        {
          title: 'slack天然沐浴用品電商網站',
          info:
            '作品的發想是有想過往電商公司做發展，作品想模擬電商網站的架構跟邏輯，透過購物車和下訂單等功能能訓練js的實務應用，也能了解大概是怎麼運作的',
          skill:
            'Vue / Bootstrap / flex / Scss / RWD / axios / promise / restful api',
          url: 'https://because-hung.github.io/vue.js-project-web/#/',
          img: '示意圖'
        },
        {
          title: '仿youtube 靜態網頁',
          info: '仿youtube ui',
          skill: 'Nuxt / Css / flex / RWD ',
          url: '作品網址',
          img: '示意圖'
        }
      ]
    }
  }
}
</script>
<style lang="scss">
body{
    background-image: url(../assets/bodyBg.jpg);
      background-size: cover;
  background-position: center center;
}
.profile {
  background-image: url(../assets/profileBg.jpg);
  background-size: cover;
  background-position: center center;
}
.blur{
  backdrop-filter: blur(6px);
}
</style>
