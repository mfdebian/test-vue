<template>
  <div>
    <!-- iteration through postsArray array -->
    <!-- iteration requires to bind a unique key -->
    <div v-bind:key="post.id" v-for="post in postsArray">
      <PostItem v-bind:post="post"
      v-on:delete-post="$emit('delete-post', post.id)" />
    </div>
  </div>
</template>

<script>
  import PostItem from './PostItem.vue';

  export default {
    name: "Posts",
    components: {
      PostItem
    } ,
    /* assing postsArray import into props
      'props' is a native property of the component */
    props: ["postsArray"]
  }
</script>

<style scoped>

</style>
