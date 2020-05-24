<template>
  <div id="app">
    <h1>{{ swiperType }}</h1>
    <img src="./assets/logo.png">
    <HomePage/>
  </div>
</template>

<script>
import HomePage from './components/HomePage';
export default {
  name: 'App',
  components: {
    HomePage
  },
  data() {
    return {
      swiperType: 'Easy Vertical Swiper'
    }
  },
}
</script>

<style>
    #app {
      font-family: 'Avenir', Helvetica, Arial, sans-serif;
      -webkit-font-smoothing: antialiased;
      -moz-osx-font-smoothing: grayscale;
      text-align: center;
      color: #2c3e50;
      margin-top: 60px;
      display: flex;
      align-items: center;
      flex-direction: column;
    }
</style>
