<template>
  <div id="app">
    <todolist></todolist>
    <header-top></header-top>
  </div>
</template>

<script>
import Header from './components/Header.vue'
import Todolist from './components/Todolist.vue'

export default {
  name: 'App',
  components: {
    'todolist': Todolist,
    'header-top': Header
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
