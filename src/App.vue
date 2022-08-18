<template>
  <div id="app">
    <the-tweets></the-tweets>
  </div>
</template>

<script>

import TheTweets from '@/components/TheTweets.vue'


export default {
  
  components: {
    TheTweets
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
