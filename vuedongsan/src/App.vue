<template>

  <div class="menu">
    <a v-for="작명 in 메뉴들" :key="작명">{{ 작명 }}</a>
  </div>

  <div class="black-bg" v-if="모달창열렸니">
    <div class="white-bg">
      <h4>상세페이지임</h4>
      <p>상세페이지 내용임</p>
      <button @click="모달창열렸니=false">닫기</button>
    </div>
  </div>

  <img src="./assets/logo.svg" alt="Vue logo" width="100px" height="100px">

  <div class="red" :style="style" v-for="(room,i) in 원룸들" :key="i">
    <img :src="원룸들[i].image" class="room-img">
    <h4 @click="모달창열렸니=true">{{ 원룸들[i].title }}</h4>
    <p>{{ 원룸들[i].price }}만원</p>
  </div>
</template>

<script>

import data from './assets/oneroom.js';

export default {
  name : 'App',
  data(){
    return {
      원룸들 : data,
      모달창열렸니 : false,
      신고수 : [0, 0, 0],
      style : 'color : blue',
      products : ['역삼동원룸', '천호동원룸', '마포구원룸'],
      메뉴들 : ['Home', 'Shop', 'About']
    }
  },
  methods: {
    increase(i) {
      this.신고수[i] += 1;
    }
  },
  components : {
  }
}
</script>

<style>
body {
  margin : 0
}
div {
  box-sizing: bordeer-box;
}
.black-bg {
  width: 100%; height: 100%;
  background: rgba(0,0,0,0.5);
  position: fixed; padding: 20px;
}
.white-bg {
  width: 100%; background: white;
  border-radius: 8px;
  padding: 20px;
}


.room-img {
  width: 100%;
  margin-top: 40px;
}
.menu {
  background: darkslateblue;
  padding: 15px;
  border-radius: 5px;
}
.menu a {
  color: white;
  padding: 10px;
}
</style>