<template>
  <div class="container mx-auto mt-12 lg:grid lg:grid-cols-12">
    <!--個人資料 -->
    <div class="profileSkill col-span-5 px-6 lg:px-0">
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
        <li class="font-bold  my-2 sm:my-8">Mail: 4a33a006@stust.edu.tw</li>
        <li class="font-bold  my-2 sm:my-8">From: Taichung, Taiwan</li>
        <li class="font-bold  my-2 sm:my-8">
          Github:
           <br>
          <a class="bg-yellow-500 sm:bg-transparent p-1 text-blue-500" href="https://github.com/because-hung">
            https://github.com/because-hung</a
          >
        </li>
        <li class="font-bold  my-8 ">
          Blog:
          <br>
          <a class="breakWord bg-yellow-500 sm:bg-transparent p-4 text-blue-500" href="https://because-hung.medium.com/">
            https://because-hung.medium.com/</a
          >
        </li>
      </ul>
    </div>
    <!--技能 -->
    <div class="skillProject  ">
      <h2 class="font-bold text-3xl mt-10 ">
        <span class="text-5xl bg-red-500 text-white p-2 mr-2 ">技能</span>
        <strong class="text-red-500 font-bold text-2xl" >SKILLS</strong>
      </h2>
      <div class="skill py-6 sm:px-6 lg:px-0 grid  grid-rows-1 grid-cols-1 sm:grid-cols-2 gap-x-5 gap-y-12">
        <div class="Css blur-sm border-b-4 border-r-4 border-gray-800 rounded-2xl   shadow-xl  p-2 ">
          <h3 class="text-2xl font-bold mb-3 lg:text-yellow-200">HTML / CSS</h3>
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
        <div class="Js blur-sm  border-b-4 border-r-4 border-gray-800 rounded-2xl shadow-xl   p-2">
          <h3 class="text-2xl font-bold mb-3 lg:text-yellow-200">JavaScript / Vue.js</h3>
          <ul class="flex flex-wrap ">
            <li
              v-for="(item, i) in jsSkill"
              :key="i"
              class="font-bold m-2 bg-green-300 w-28 rounded-full p-2"
            >
              {{ item }}
            </li>
          </ul>
        </div>
        <div class="Other blur-sm border-b-4 border-r-4 border-gray-800 rounded-2xl  shadow-xl  p-2">
          <h3 class="text-2xl font-bold mb-3 lg:text-yellow-200">Other Skill</h3>
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
        <div class="Someskill blur-sm border-b-4 border-r-4  border-gray-800 rounded-2xl  shadow-xl  p-2">
          <h3 class="text-2xl font-bold mb-3 lg:text-yellow-200">略懂</h3>
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
    <div class="projectInfo col-span-7 sm:ml-6 mb-10">
    <div class="project font-bold text-xl mt-6 ">
      <div class="projectTitle mb-8">
        <span class="text-5xl bg-red-500 text-white p-2 mr-2 ">作品 </span>
        <strong class="text-red-500 font-bold text-2xl ">PROJECT</strong>
        </div>
        <div class="projectCard px-8 sm:px-12 font-medium text-left ">
          <ul
            class=" flex flex-col  py-8 blur ring ring-offset-4 ring-gray-600 text-white p-6 rounded-2xl"
            v-for="(item, i) in project"
            :key="i"
          >
            <li class="mt-4 mb-6 ">
               <span class="bg-blue-700 p-2 text-white font-bold ">{{ item.title }}</span>
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
            <li class="my-6 ">作品網址 <a class="p-1 bg-yellow-300 text-blue-600" :href="item.url"> {{item.url}}</a></li>
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
          title: 'slack 天然沐浴用品電商網站',
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
