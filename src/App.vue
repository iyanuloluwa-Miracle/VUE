<template>
  <div id="app">
    <h2>Volume Tracker(0-20)</h2>
    <h3>Current Volume - {{ volume }}</h3>
    <div>
      <button @click="volume +=2">Increase</button>
      <button @click="volume -=2">decrease</button>
    </div>

    <input type="text" v-model="movie" >
    <input type="text" v-model="movieInfo.title" >
    <input type="text" v-model="movieInfo.actor" >

  </div>
 
  
</template>

<script>
export default {
  name: "App",
  data() {
    return {
      volume: 0,
      movie: 'Batman',
      movieInfo: {
        title: '',
        actor:''
      }
    };
  },
  methods: {},
  computed: {},
  watch: {
    volume(newValue, oldValue) {
      if (newValue > oldValue && newValue === 16) {
        alert('Listening to a high volume for a long time may damage your hearing');
      }
    },
    movie: {
      handler(newValue) {
        console.log(`Calling API with name=${newValue}`);
      },
      immediate: true,
      //deep: true // Assuming movie is an object and you want to watch for nested changes
    }
  },
  movieInfo:{
    handler(newValue){
      console.log(
        `Calling API with movie title = ${newValue.title} and actor = ${newValue.actor}`
      )

    },
    deep: true
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
