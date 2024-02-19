<template>
  <div id="app">
    <h4>App Component Text</h4>
    <ChildStyles>
      <h4>Childstyles component text</h4>
    </ChildStyles>
     

  </div>
</template>

<script>
//import Card from './components/Card.vue';
//import NameList from './components/NameList.vue';
import ChildStyles from './components/childStyles.vue';


export default {
  name: "App",
  components:{
    
    ChildStyles
    
  },


  data(){

  },
  methods:{

  }

  
  
};
</script>

<style scoped>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  text-align: center;
  color: rgb(130, 184, 238);
  margin-top: 100px;
}
h4{
  color: orange; 
}
</style>
