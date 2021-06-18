<template>

  <div class="menu">
    <a v-for="a, in menu" :key="a">{{a}}</a>
    <!-- key는 반복문 돌린 요소를 컴퓨터가 구분하기 위해 쓴다. -->
  </div>

  <div v-for="product in products" :key="product">
    <h4>{{product}}</h4>
    <p>50 만원</p>
    <button v-on:click="accusecount++">허위매물신고</button> <span>신고수 : {{ accusecount }}</span>
    <!-- v-on:click 또는 @click으로도 가능 -->
  </div>
</template>



<script>

export default {
  name: 'App',
  data(){
    return{
      accusecount : 0,
      menu : ['Home', 'Shop', 'About'],
      products : ['역삼동원룸', '천호동원룸', '마포구원룸']
    }
  },
  components: {
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
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
