

<template>
  <h1>ButtonView</h1>
  <ButtonBar @radioChanged="onRadioChanged"  :Artists=Artists ></ButtonBar>
   <h4> Radio now playing: {{RadioNowPlaying}}</h4>
 </template>

<script>
import ButtonBar from '../components/ButtonBar.vue'


export default {
  name: 'ButtonView',
  components: {
    ButtonBar
  },
   data() {
    return {
      radioValue:0,
      Artists:[]
    }
 },
  methods: {
      onRadioChanged(radiovalue) {
        this.radioValue=radiovalue
      }
  },
  computed: {
      RadioNowPlaying() {
        return this.Artists[this.radioValue-1];
      }
  },
   created() {

    fetch("http://localhost:3000/Artist",)
      .then(respons=> respons.json() )
      .then(data=> {
          this.Artists=data.map(m=>m.name);
      } )
      .catch(e=>console.log(e))
      .finally( ()=> {
        console.log('Artists from json server:'+this.Artists)
      });
  }
}
</script>

<style scope>

</style>