<template>
  <h2>Fullname: {{ fullName }} </h2>
  <h2>total computed: {{ total }}</h2>
  <h2>total method: {{ getTotal() }}</h2>
  <input type="text" v-model.number="items[1].price">

  <template v-for="item in items" :key="item">
    <h2 v-if="item.price>100"> {{item.title}} </h2>
  </template>

  <template v-for="item in expensiveItem" :key="item">
    <h2> {{item.title}} </h2>
  </template>
</template>

<script>


export default {
  name: 'App',
  data() {
    return {
      firstName: 'Pham',
      lastName: 'Toai',
      items: [
        {
          id: 1,
          title: 'TV',
          price: 120,
        },
        {
          id: 2,
          title: 'Phone',
          price: 220,
        },
        {
          id: 3,
          title: 'Laptop',
          price: 40,
        },
      ],
      country: ''
    };
  },
  methods: {
    getTotal() {
      console.log("method");
      return this.items.reduce((total, curr) => (total = total + curr.price), 0)
    }
  },
  computed: {
    fullName() {
      return `${this.firstName}  ${this.lastName}`
    },
    total() {
      console.log("computed");
      return this.items.reduce((total, curr) => (total = total + curr.price), 0)
    },
    expensiveItem() {
      return this.items.filter(item => item.price > 100)
    }
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  /* text-align: center; */
  color: #2c3e50;
  margin-top: 60px;
}


</style>
