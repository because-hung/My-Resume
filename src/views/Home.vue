<template>
  <div class="container mx-auto mt-12  text-left">
    <h1 class="text-5xl font-bold ml-12 mb-6">洪瑛蔚</h1>
    <hr class="border-2 " />
    <div class="img"></div>
    <!--個人資料 -->
    <div class="profile mb-4">
      <h2 class="font-bold text-3xl my-4">個人資料 <strong class="text-red-500 font-bold text-2xl">PROFILE</strong></h2>
      <hr class="border-2 mb-4" />
      <ul>
        <li>Mail: 4a33a006@stust.edu.tw</li>
        <li>Taichung, Taiwan</li>
        <li>
          Github:
          <a href="https://github.com/because-hung"
            >https://github.com/because-hung</a
          >
        </li>
      </ul>
    </div>
      <!--技能 -->
    <hr class="border-2" />
       <h2 class="font-bold text-3xl my-4">技能 <strong class="text-red-500 font-bold text-2xl">SKILLS</strong></h2>
      <hr class="border-2 mb-4" />
       <div class="skill mb-4">
      <div class="Css">
         <h3 class="text-2xl font-bold">HTML / CSS </h3>
      <ul v-for="(item, i) in cssSkill" :key="i">
        <li>{{ item }}</li>
      </ul>
      </div>
      <div class="Js">
      <h3 class="text-2xl font-bold">JavaScript / Vue.js </h3>
      <ul v-for="(item, i) in jsSkill" :key="i">
        <li>{{ item }}</li>
      </ul>
      </div>
      <div class="Other">
        <h3 class="text-2xl font-bold">Other Skill </h3>
      <ul v-for="(item, i) in otherSkill" :key="i">
        <li>{{ item }}</li>
      </ul>
      </div>
      <div class="Someskill">
           <h3 class="text-2xl font-bold">略懂 (有使用過, 但還沒有很熟練)</h3>
      <ul v-for="(item, i) in knowSomeSkill" :key="i">
        <li>{{ item }}</li>
      </ul>
      </div>
    </div>
      <!--作品 經歷 -->
    <div class="project"></div>
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
        'Jquery',
        'ES5 / ES6',
        'promise / async/await'
      ],
      otherSkill: [
        'Webpack (懂運作,不會配置)',
        'Git',
        'Zeplin'
      ],
      knowSomeSkill: [
        'Vuex',
        'Webpack 5',
        'React'
      ],
      project: [
        {
        }
      ]
    }
  }
}
</script>
