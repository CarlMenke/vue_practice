<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <GoodComponent msg='hello'/>
    <RightPart number= 10 />
    <LeftPart image = '../assets/logo/png'></LeftPart>
  </div>
</template>

<script>
import GoodComponent from './components/GoodComponent.vue';
import RightPart from './components/RightPart.vue'
import LeftPart from './components/LeftPart.vue'

export default {
  name: 'App',
  components: {
    RightPart,
    GoodComponent,
    LeftPart
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
