<template>
  <h2>Fullname: {{ fullName }} </h2>
  <h2>total: {{ total }}</h2>
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
          price: 100,
        },
        {
          id: 2,
          title: 'Phone',
          price: 220,
        },
        {
          id: 3,
          title: 'Laptop',
          price: 400,
        },
      ]
    };
  },
  methods: {
    
  },
  computed: {
    fullName() {
      return `${this.firstName}  ${this.lastName}`
    },
    total() {
      return this.items.reduce((total, curr) => (total = total + curr.price), 0)
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
