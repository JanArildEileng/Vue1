<template>

   <Navigasjonsbar></Navigasjonsbar>
   <div id="rv">
     <router-view ></router-view>
   </div> 
   <Footer></Footer>
 
</template>

<script>
import Navigasjonsbar from './components/Navigasjonsbar.vue'
import Footer from './components/Footer.vue'

export default {
  name: 'App',
  components: {
    Navigasjonsbar,Footer
  },

   //lifecyclehooks
   created() {
    console.log('App created')
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
  margin-top: 10px;
  background-color: darkseagreen;
  
}
#rv {
    min-height: 400px;

    background-color: cornsilk;
}

</style>
