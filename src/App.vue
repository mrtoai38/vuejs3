
<template>
    <h2>Volume tracker (0-20)</h2>
    <h3>Current Volume - {{ volume }}</h3>
    <div>
      <button @click="volume += 2">Increase</button>
      <button @click="volume -= 2">Decrease</button>
    </div>
    <input type="text" v-model="movie">
    <input type="text" v-model="movieInfor.title">
    <input type="text" v-model="movieInfor.actor">
    <div>
      <button @click="movieList = movieList.concat(['wonderwoman'])">Add movie</button>
    </div>
</template>

<script>


export default {
  name: 'App',
  data() {
    return {
      volume: 0,
      movie: 'batman',
      movieInfor: {
        title: '',
        actor: ''
      },
      movieList: ['Batman', 'superman']
    }
  },
  methods: {},
  computed: {},
  watch: {
    volume(newValue, oldValue) {
      if(newValue > oldValue && newValue == 16) {
        alert('Listening to a high volume for a long time may damage your hearing');
      }
    },
    movie:{
      handler(newValue) {
        console.log(`Calling API with movie name = ${newValue}`);
      },
      immediate: true
    },
    movieInfor: {
      handler(newValue) {
        console.log(`Calling API with movie title = ${newValue.title} and actor = ${newValue.actor}`);
      },
      deep: true
    },
    movieList: {
      handler(newValue) {
        console.log(`Update list ${newValue}`);
      },
      // deep: true
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
