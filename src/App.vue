<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <HelloWorld msg="Welcome to Your Vue.js App" message="ya3tiik 3assba"/>
    <HelloWorld msg="Welcome to Your 9o7b app" message="ya3tiik essa7a"/><br>
    <cars name="peugeot" modele= "206" year="2023"/>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import Cars from './components/Cars.vue'

export default {
  name: 'App',
  components: {
    HelloWorld,
    Cars
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
