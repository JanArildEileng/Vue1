<template>
  <div class="ButtonBar">
     


    <h3>Pushed:{{ buttonClickedMessage }}   radio={{radioValue}}</h3>
     
    <h5>Button</h5>
    <button v-on:click="clickB1(item)"  v-for=" (item,name) in names" :key="name" >
        {{item.name}}
    </button>  

    <h5>Radio</h5>
  
    <label class="label1"   v-for="(item,index) in Artists" :key="index">
       <input type="radio" name="radiogruppe1" v-bind:value="index+1" v-model="radioValue"  v-bind:id="item.id"  @change="$emit('radioChanged',radioValue)"  >
       {{item}}

    </label>
   


  
    <h5>Checkbox</h5>
    <label v-for=" (item,name) in names" :key="name" >
      {{item.name}}
       <input type="checkbox"  v-model="item.checked" v-bind:id="item.id"  >
    </label>
   

  </div>
</template>

<script>
export default {
  name: 'ButtonBar',
  props: {
      Artists:Array
  },
  emits: ['radioChanged'],

  data() {
    return {
      radioValue:2,

      buttonClickedMessage: '',
      names:[  {name:'Button-1',checked:true}, {name:'Button-2',checked:false}, {name:'Button-3',checked:false}]
    }
  },

  methods: {
      clickB1(buttonPushed) {
      console.log(buttonPushed.name+" "+buttonPushed.checked);
      
      let checked=buttonPushed.checked?buttonPushed.checked:'false'
      
      this.buttonClickedMessage = buttonPushed.name+" "+checked
    }
  },
  computed: {
      
  },
   created() {
    this.$emit('radioChanged',this.radioValue);
  }

}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

 .label1  {
   margin-right: 10px;
 }

div {
  background-color:beige;
}
button {
  background-color: lawngreen;
  height: 5.0ex;
}

h5 {
  text-align: left;
  margin-left: 40px;
  color: black;
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
