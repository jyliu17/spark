<template>
   <div>
       <div v-for="post in posts" :key="post.id">
            <PostDetail :id= post.id :title= post.title :body= post.body />
       </div>
   

   </div>
</template>

<script>
import axios from "axios"
import PostDetail from './PostDetail.vue'


export default {
    name: 'PostList',
    data() {
        return {
            posts: [],
        }
    },
    methods: {
        getPosts(){
            axios.get('https://jsonplaceholder.typicode.com/posts')
            .then((response) => {
                console.log(response.data)
                this.posts = response.data
            })
            .catch((error)=> {
                console.log(error)
            })
        }
    },
    created(){
            this.getPosts()
    },
    components: { PostDetail }
}

</script>

<style scoped>
    header {
        display: flex;
        justify-content: space-between;
        align-items: center;
        margin-bottom: 10px;
    }

</style>
