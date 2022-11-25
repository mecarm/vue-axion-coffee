<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <MainComp/>
  </div>
</template>

<script>
import MainComp from './components/MainComp.vue'

export default {
  name: 'App',
  components: {
    MainComp
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
</style>
