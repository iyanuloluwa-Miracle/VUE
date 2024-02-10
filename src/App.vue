<template>
  <div id="app">
    <GreetMessage></GreetMessage>
  </div>
</template>

<script>
import GreetMessage from './components/GreetMessage.vue';

export default {
  name: "App",
  components:{
    GreetMessage
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
