<template>
  <div>
    <h2>Computed fullname - {{ fullName }}</h2>
    <button @click="items.push({ id: 1, title: 'keyboard', price: 5 })">
      Add Item
    </button>
    <h2>Computed Total - {{ total }}</h2>
    <h2>Method Total - {{ getTotal() }}</h2>
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

    }
  },
  computed: {
    fullName() {
      return `${this.firstName} ${this.lastName}`;
    },
    total() {
      return this.items.reduce((total, curr) => total + curr.price, 0);
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
