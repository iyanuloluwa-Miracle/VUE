<template>
  <div id="app">
    <PostList/>
    

  </div> 
</template>

<script>

import PostList from './components/PostList.vue';
export default {
  name: "App",
  components:{
    PostList

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
