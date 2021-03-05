

<template>
  <h1>Home Page</h1>
  <Test1 msg="Welcome Test1"/>
 </template>

<script>
import Test1 from '../components/Test1.vue'

export default {
  name: 'Home',
  components: {
    Test1
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