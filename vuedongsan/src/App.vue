<template>

<div class="menu">
  <a v-for="작명 in 메뉴들" :key="작명">{{ 작명 }}</a>
  
</div>

  <img src="./assets/logo.svg" alt="Vue logo" width="100px" height="100px">

  <div v-for="(p, i) in products" :key="i">
    <h4 class="red" :style="style">{{ p }}</h4>
    <p>XX 만원</p>
  </div>
</template>

<script>
export default {
  name : 'App',
  data(){
    return {
      style : 'color : blue',
      products : ['역삼동원룸', '천호동원룸', '마포구원룸'],
      메뉴들 : ['Home', 'Shop', 'About']
    }
  },
  components : {
  }
}
</script>

<style>
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