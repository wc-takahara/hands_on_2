<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <h3>ハンズオン</h3>
    <Qusetion/>
  </div>
</template>

<script>
import Qusetion from './components/answer/question-9.vue'

export default {
  name: 'App',
  components: {
    Qusetion
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
