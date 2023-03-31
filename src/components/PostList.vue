<template>
    <div>
        <button @click="getPosts">Load posts</button>
        <h3 v-if="errMsg">{{ errMsg }}</h3>
        <div v-for="post in posts" :key="post.id">
            <h3>{{ post.id }}. {{ post.title }}</h3>
            <p>{{ post.body }}</p>
            <hr>
        </div>
        
    </div>
</template>

<script>
    import axios from 'axios';
    export default {
        name: 'PostList',
        data() {
            return {
                posts: [],
                errMsg: ''
            }
        },
        methods: {  
            getPosts(){
                console.log("methods get post >>>");
                axios.get('https://jsonplaceholder.typicode.com/posts')
                    .then((res)=> {
                        console.log(res.data);
                        this.posts = res.data;
                    })
                    .catch((err)=> {
                        console.log(err);
                        this.errMsg = err;
                    })
            }
        }
    }
</script>

<style scoped>
h3 {
    color: red;
}
</style>