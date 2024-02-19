<template>
  <div id="app">
    <NameList>
      <template v-slot:default="slotProps">
        {{ slotProps.firstName }} {{ slotProps.lastName }}

      </template>
      
    </NameList> 


    <NameList>
      <template v-slot:default="slotProps">
        {{ slotProps.firstName }} {{ slotProps.lastName }}

      </template>
      
    </NameList>

    <NameList>
      <template v-slot:default="slotProps">
        {{ slotProps.lastName }}

      </template>
      
    </NameList> 

    <NameList>
      <template v-slot:default="slotProps">
        {{ slotProps.firstName }}

      </template>
      
    </NameList> 
  </div>
</template>

<script>
//import Card from './components/Card.vue';
import NameList from './components/NameList.vue';

export default {
  name: "App",
  components:{
    
    NameList
    
  },


  data(){

  },
  methods:{

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
