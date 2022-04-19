<template>
  <div id="app">
    
    <TweetContainer/>
  </div>
</template>

<script>
import TweetContainer from "./components/TweetContainer.vue"

export default {
  name: 'App',
  components: {
      TweetContainer
}
}
</script>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
html{
  background-color: blanchedalmond;
  margin: 0;
  padding: 0;
}

</style>
