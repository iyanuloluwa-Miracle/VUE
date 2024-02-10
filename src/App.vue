<template>
  <div id="app">
    <GreetMessage name="Kent" heroName="Superman"/>
    <GreetMessage name="Bruce" heroName="Batman"/>
    <GreetMessage name="Barry Allen" heroName="The Flash"/>
    <GreetMessage :name="name" :heroName="channel"/>
  </div>
</template>

<script>
import GreetMessage from './components/GreetMessage.vue';

export default {
  name: "App",
  components:{
    GreetMessage
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
  color: peru;
  margin-top: 100px;
}
</style>
