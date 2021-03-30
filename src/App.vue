<template>
  <AppView></AppView>
  <!-- <img alt="Vue logo" src="./assets/logo.png"> -->
  <!-- <HelloWorld msg="Welcome to Your Vue.js App"/> -->
</template>

<script>
// import HelloWorld from './components/HelloWorld.vue'

import AppView from './components/App-View.vue'

export default {
  name: 'App',
  components: {
    AppView
  }
}
</script>

<style>
body {
  background: #121212;
}
#app {
  font-weight: bold;
  color: #898989;
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}
</style>
