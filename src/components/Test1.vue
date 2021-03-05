<template>
  <div class="hello test1">
    <h3>{{ msg }}</h3>
    <ButtonBar></ButtonBar>  
    <h3>{{ message }}</h3>
   </div>
</template>

<script>
import ButtonBar from './ButtonBar.vue'

export default {
  name: 'Test1',
  props: {
    msg: String
  },
  data() {
    return {
      message: 'Hello Vue.js!'
    }
  },

  methods: {
  },
    components: {
    ButtonBar
  }

}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
div {
  background-color:beige;
}
button {
  background-color: lawngreen;
  height: 5.0ex;
}


h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
