<template>
  <img src="./assets/logo.svg" alt="Vue logo">
  <div>
    원룸샵
    <h4 class="red" :style="style">{{products[0]}} 원룸</h4>
    <p>{{price1}} 만원</p>
  </div>
  <div>
    <h4>{{products[1]}} 원룸</h4>
    <p>{{price2}} 만원</p>
  </div>
  <div>
    <h4>{{products[2]}} 원룸</h4>
    <p>가격은아무거나</p>
  </div>
</template>

<script>
export default {
  name : 'App',
  data(){
    return {
      price1 : 60,
      price2 : 70,
      style : 'color : blue',
      products : ['역삼동원룸', '천호동원룸', '마포구원룸']
    }
  },
  components : {
  }
}
</script>

<style>
</style>