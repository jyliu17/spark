<template>
  <div class="container">
    <HeaderComp title= "Top 100 Quotes" />
    <PostList />
  </div>
</template>

<script>


import PostList from './components/PostList.vue'
import HeaderComp from './components/HeaderComp.vue'


export default {
    name: "App",
    
    components: { 
      HeaderComp, 
      PostList 
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
