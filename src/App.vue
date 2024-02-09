<template>
  <div id="app">
    <h2>Volume Tracker(0-20)</h2>
    <h3>Current Volume - {{ volume }}</h3>
    <div>
      <button @click="volume +=2">Increase</button>
      <button @click="volume -=2">decrease</button>
    </div>

  </div>
 
  
</template>

<script>
export default {
  name: "App",
  data() {
    return {
      volume: 0
    };
  },
  methods: {},
  computed: {},
  watch:{
    volume(newValue, oldValue){
      if(newValue > oldValue && newValue === 16){
        alert('listening to a high volume for a long time may damage your hearing')
      }

    }
  }
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  text-align: center;
  color: #2c3e50;
  margin-top: 100px;
}
</style>
