<template>
  <div>
    <input type="text" v-model="name">
    <Card>{{ name }}</Card>
    <Card>{{ name }}</Card>
    <Card></Card>

    <Card>
      <template v-slot:header>
        <h3>header</h3>
      </template>
      <template v-slot:default>
        <img src="https://picsum.photos/200" alt="">
      </template>
      <template v-slot:footer>
        <button>View Details</button>
      </template>
    </Card>

    <NameList/>
  </div>
</template>

<script>
import Card from './components/Card.vue';
import NameList from './components/NameList.vue';

export default {
  name: 'App',
  components: {
    Card,
    NameList
  },
  data() {
    return {
     name: ''
    }
  },
  methods: {
    
  },
  computed: {},
  watch: {},
  provide() {
    return {
      
    }
  }
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
