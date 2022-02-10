<template>
  
  <main>
    <div class="container">
       
       <h1>i miei post</h1>

        <PostItem 
          v-for="post in posts"
          :key="post.id"
          :post="post"
        />

    </div>
  </main>

</template>

<script>

import PostItem from './partials/PostItem';

export default {
  name: 'Posts',
  components: {
    PostItem
  },
  data(){
    return{
      apiUrl: 'http://127.0.0.1:8000/api/posts',
      posts: null
    }
  },
  mounted(){
    this.getPosts(this.apiUrl);
  },
  methods:{
    getPosts(){
      axios.get('')
      .then(res => {
        this.posts = res.data
        console.log(this.posts);
      })
    }
  }
}
</script>

<style lang="scss" scoped>
main{
  padding: 30px 0;
  h1{
    margin-bottom: 20px;
  }
}

</style>