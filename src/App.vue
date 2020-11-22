<template>
  <div id="app">
    <Recipe />
  </div>
</template>

<script>
import Recipe from './components/Recipe.vue'

export default {
  name: 'app',
  components: {
    Recipe
  }
}
</script>

<style>
body {
background: #10d6b4;
}

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2209a1;
  margin-top: 60px;
}
</style>
