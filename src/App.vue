<template>
  <div id="app">
    <div class="logo">
      <img src="https://i.pinimg.com/originals/fa/16/ec/fa16ec19e6212b6c68daeea1b06f4a52.png" alt="">
    </div>
    <div class="cards">
      <MainComp v-for="(element, index) in dataCoffee" :key="index" :dettaggliCoffe="element"/>
    </div>
  </div>
</template>

<script>
import axios from 'axios'
import MainComp from './components/MainComp.vue'

export default {
  name: 'App',
  components: {
    MainComp
  },
  data() {
    return{
      dataCoffee: ''
    }
  },
  mounted(){
    axios.get('https://api.sampleapis.com/coffee/hot')
      .then ( (response) =>{
        this.dataCoffee = response.data
      })
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

  .logo{
    width: 200px;
  }
  img{
    width: 100%;
  }
}
.cards{
  width: 80%;
  margin: 20px auto;
  display: flex;
  flex-wrap: wrap;
}
</style>
