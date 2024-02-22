<template>
  <div id="app">
    <ClickCounter/>
    <HoverCounter/>
  </div> 
</template>

<script>

//import PostList from './components/PostList.vue';
import ClickCounter from './components/ClickCounter.vue';
import HoverCounter from './components/HoverCounter.vue';


export default {
  name: "App",
  components:{
    ClickCounter,
    HoverCounter
    

  },


  
  

  
  
};
</script>

<style scoped>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  text-align: center;
  color: rgb(130, 184, 238);
  margin-top: 100px;
}

</style>
