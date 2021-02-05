<template>
  <News v-bind:news="news"/>
</template>

<script>
import axios from 'axios';
import News from './components/News.vue'

export default {
  name: 'App',
  components: {
    News
  },
  data(){
    return {
      news: []
      }
  },
  async created() {
    const response = await axios.get("https://newsapi.org/v2/top-headlines?country=us&apiKey=e446a7bb80ec4d58b4c84fa7c257789b");
    this.news = response.data.articles;
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
  margin-top: 60px;
}
</style>
