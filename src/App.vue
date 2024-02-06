<template>
  <div>
    <h2 v-for="(name,index) in names" :key="name"> {{index}} {{ name }}</h2>
    <h2 v-for="name in fullNames" :key="name.first">{{ name.first }} {{ name.last }}</h2>
    <div v-for="actor in actors" :key="actor.name">
      <h2>{{ actor.name }}</h2>
      <h3 v-for="movie in actor.movies" :key="movie">{{ movie }}</h3>
    </div>
  </div>


</template>


<script>
export default {
  name: "App",
  data() {
    return {
      names:['Bruce', 'Clark', 'Diana'],
      fullNames:[
        {first:'Dina', last:'Iyanuloluwa'},
        {first:'Dina', last:'Anuoluwapo'},
        {first:'Dina', last:'Miracle'}
      ],
      actors:[
        {
          name:'Christian Bale',
          movies:['Batman','The prestige']
        },
        {
          name:'Di caprio',
          movies:['Titanic','Inception']
        },
      ]
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
