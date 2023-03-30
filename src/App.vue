<template>
    <h2>{{name}}</h2>
    <div>
      <button v-on:click="changeName">Change name</button>
    </div>
    <h2>{{count}}</h2>
    <div>
      <button v-on:click="increment($event), changeName($event)">Increment</button>
      <button @click="decrement">Decrement</button>
    </div>
</template>

<script>


export default {
  name: 'App',
  data() {
    return {
      name: 'Toaiben',
      count: 0,
    };
  },
  methods: {
    changeName(event) {
      this.name = 'quyetben';
      console.log('Event c:', event);
    },
    increment(event) {
      this.count++;
      console.log('Event:', event);
    },
    decrement() {
      this.count--;
    }
  },
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}


</style>
