<template>
  <div id="app">
    <button @click="activeTab = 'TabA'">Tab A</button>
    <button @click="activeTab = 'TabB'">Tab B</button>
    <button @click="activeTab = 'TabC'">Tab C</button>

    <keep-alive>
      <component :is="activeTab" />
    </keep-alive>
    

  </div> 
</template>

<script>
//import Card from './components/Card.vue';
//import NameList from './components/NameList.vue';
//import ChildStyles from './components/childStyles.vue';
import TabA from './components/TabA.vue';
import TabB from './components/TabB.vue';
import TabC from './components/TabC.vue';

export default {
  name: "App",
  components:{
    
    TabA,
    TabB,
    TabC,
    
  },


  data(){
    return{
      activeTab: 'TabA',
      
      

    }

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
