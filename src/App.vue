<template>
  <div>
    <div v-for="name in names" :key="name">
      <h2 v-if="name === 'Bruce'">{{ name }}</h2>
    </div>
  </div>
</template>



<script>
export default {
  name: "App",
  data() {
    return {
      names:['Bruce', 'Clark', 'Diana'],
      
    };
  },
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
