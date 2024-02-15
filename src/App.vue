<template>
  <div id="app">
    <articlesComponent id="my-article" title="Article Title" :likes="50" :isPublished="true"/>
  </div>
</template>

<script>
//import GreetMessage from './components/GreetMessage.vue';
import articlesComponent from './components/articlesComponent.vue';

export default {
  name: "App",
  components:{
    //GreetMessage,
    articlesComponent
  },
  data(){
    return{
      name:"Nikki",
      channel:'Codeevolution'
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
