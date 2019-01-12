<template>
  <div id="app">
    <img src="./assets/logo.png">
    <only_calc/>
  </div>
</template>

<script>
import only_calc from './components/only_calc'

export default {
  name: 'App',
  components: {
    only_calc,
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
