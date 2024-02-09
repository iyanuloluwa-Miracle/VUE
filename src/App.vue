<template>
  <div>
    <h2>Computed fullname - {{ fullName }}</h2>
    <button @click="changeFullName">Change fullName</button>
    
    
    
    <button @click="items.push({ id: 1, title: 'keyboard', price: 5 })">
      Add Item
    </button>
    <h2>Computed Total - {{ total }}</h2>
    <h2>Method Total - {{ getTotal() }}</h2>


    <div v-for="item in items" :key="item.id">
      <h2 v-if="item.price > 100">{{ item.title }} {{ item.price }}</h2>
    </div>

    <div>
      <h2 v-for="item in expensiveItems" :key="item.id"> {{ item.title }} {{ item.price }}</h2>
    </div>

    

    
  </div>
  
</template>

<script>
export default {
  name: "App",
  data() {
    return {
      firstName: "Bruce",
      lastName: "Wayne",
      items: [
        {
          id: 1,
          title: "Tv",
          price: 100,
        },
        {
          id: 2,
          title: "phone",
          price: 200,
        },
        {
          id: 3,
          title: "Laptop",
          price: 300,
        },
      ],
    };
  },
  methods: {
    getTotal(){
      return this.items.reduce((total, curr) => total + curr.price, 0);

    },

    changeFullName(){
        this.fullName = 'Clark Kent'

      }
  },
  computed: {
    fullName: {
      get() {
        return `${this.firstName} ${this.lastName}`;
      },
      set(value) {
        const names = value.split(' ')
        this.firstName = names[0]
        this.lastName = names[1]

      },
     
     
    },
    total() {
      return this.items.reduce((total, curr) => total + curr.price, 0);
    },
    expensiveItems() {
      return this.items.filter((item) => item.price > 100);
    },
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
</style>
