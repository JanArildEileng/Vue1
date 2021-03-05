
<template>
  <h1 class="title">About Page</h1>
  <HelloWorld msg="Welcome to My Vue.js App"/>
  
</template>

<script>
import HelloWorld from '../components/HelloWorld.vue'

export default {
  name: 'About',
  components: {
    HelloWorld
  }
}
</script>

<style scope>
 
 .title {
     color: lawngreen;
 } 


</style>