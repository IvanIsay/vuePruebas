

<template>
  <div id="app">
     <h1> Soy la plantilla VUE </h1>
     <Test/>
     <Users/>
  </div>
</template>



<script>
  import Test from './components/test.vue'
  import Users from './components/users.vue'
export default {
  name: 'App',
  components: { Test,Users }
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
