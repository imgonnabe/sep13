<template>
  <!--<HelloWorld msg="Welcome to Your Vue.js App"/>-->
  <DivBox></DivBox>
  <DivBox></DivBox>
  <SoundOne></SoundOne>
  <BoardVue></BoardVue>
</template>

<script>
// import HelloWorld from './components/HelloWorld.vue'
import BoardVue from './components/BoardVue.vue'
import SoundOne from './components/SoundOne.vue'
import DivBox from './components/DivBox.vue'

export default {
  name: 'App',
  components: {
    // HelloWorld
    BoardVue, SoundOne, DivBox
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
