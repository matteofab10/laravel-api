<template>
  
  <article>
    <h3>
      <a href="#">{{post.title}}</a>
    </h3>
    <p class="date">{{ post.created_at }}</p>
    <p class="text">{{ post.content }}</p>
  </article>

</template>

<script>
export default {
  name: 'PostItem',
  props: {
    'post': Object
  }
}
</script>

<style lang="scss" scoped>
  article{
    margin-bottom: 20px;
    .date{
      font-size: 12px;
      font-style: italic;
    }
    .text{
      padding: 5px 0;
    }
    a{
      color: black;
      text-decoration: none;
      &:hover{
        text-decoration: underline;
      }
    }
  }
</style>