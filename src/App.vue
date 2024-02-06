<template>
  <div>
    <h2>{{name}}</h2>
    <div>
      <button v-on:click="changeName">Change name</button>
    </div>
    <h2>{{ count }}</h2>
    <div>
      <button @click="increment(1)">Increment 1</button>
      <button @click="increment(5)">Increment 5</button>
      <button @click="decrement(1)">Decrement 1</button>
      <button @click="decrement(5)">Decrement 5</button>

    </div>
  </div>
</template>



<script>
export default {
  name: "App",
  data() {
    return {
      name:"Iyanu",
      count:0     
    };
  },
  methods:{
    increment(num){
      this.count +=num
    },
    decrement(num){
      this.count -=num
    },
    changeName(){
      this.name = 'Batman'
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
