<template>
  <PostList/>
  <CreatePost/>
</template>

<script>
import CreatePost from './components/CreatePost.vue';
import PostList from './components/PostList.vue';
export default {
  name: 'App',
  components: {
    PostList,CreatePost
  },
  data() {
    return {
      
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
