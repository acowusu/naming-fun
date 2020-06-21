<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo1.svg" height="100px">
    <HelloWorld />
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
// import sassStyles from './main.module.sass'

export default {
  name: 'App',
  components: {
    HelloWorld
  }
}
</script>

<style>
body, html{
  /* background: #7efff5; */
}
img{
  margin: 1em
}
#app {
  /* background: #7efff5; */
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
