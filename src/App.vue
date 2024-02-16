<template>
  <div id="app">
    <Card></Card>
    <Card>Card Content</Card>
    <Card>
      <h2>Card Content</h2>
    </Card>
    <Card>
      <img src="https://picsum.photos/200"/>
    </Card>
    <Card>
      <template v-slot:header>
        <h3>Header</h3>

      </template>
      <template v-slot:default>
        <img src="https://picsum.photos/200"/>
        

      </template>
      <template v-slot:footer>
       <button>View Details</button>

      </template>
      
    </Card>
  </div>
</template>

<script>
import Card from './components/Card.vue';

export default {
  name: "App",
  components:{
    Card,
    
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
