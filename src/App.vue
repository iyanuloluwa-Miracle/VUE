<template>
  <div id="app">
    <button @click="showPopup = true">Show Popup</button>
    <Popup v-show="showPopup" @close="showPopup = false"/>
  </div>
</template>

<script>
//import GreetMessage from './components/GreetMessage.vue';
//import articlesComponent from './components/articlesComponent.vue';
import Popup from './components/Popup.vue'


export default {
  name: "App",
  components:{
    //GreetMessage,
    Popup


  },
  data(){
    return{
      showPopup: false
    }
  },
  methods:{
    closePopup(name){
      this.showPopup = false
      console.log('name',name)
    }
  }
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  text-align: center;
  color: rgb(130, 184, 238);
  margin-top: 100px;
}
</style>
