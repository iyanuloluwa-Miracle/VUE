<template>
  <div>
    <h2>{{  2 + 3 + 5 }}</h2>
    <h2>{{  5 + 13 - 15 }}</h2>
    <h2>Add method - {{ add(2,3,4,) }}</h2>
    <h2>Add method - {{ add(10,12,13) }}</h2>
  </div>
</template>



<script>
export default {
  name: "App",
  data() {
    return {      
    };
  },
  methods:{
    add(a, b, c){
      return a + b + c
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

.underline {
  text-decoration: underline;
}

.promoted {
  font-style: italic;
}

.new {
  color: crimson;
}
.sold-out {
  color: blue;
}
</style>
