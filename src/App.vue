<template>
  <div id="app">
    <PostList/>
    <CreatePost/>
    

  </div> 
</template>

<script>

import PostList from './components/PostList.vue';
import CreatePost from './components/CreatePost.vue';
export default {
  name: "App",
  components:{
    PostList,
    CreatePost

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
