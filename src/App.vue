<template>
  <div id="app">
    <Autocomplete></Autocomplete>
  </div>
</template>

<script>

import Autocomplete from './components/city-auto-complete/autocomplete.vue'

export default {
  name: 'App',
  components: {
    Autocomplete
  }
}
</script>

<style lang="less">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
