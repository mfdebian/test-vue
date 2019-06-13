<template>
  <div>
    <!-- iteration through postsArray array -->
    <!-- iteration requires to bind a unique key -->
    <div v-bind:key="post.id" v-for="post in postsArray">
      <h2>{{ post.title }}</h2>
      <h3>{{ post.body }}</h3>
    </div>
  </div>
</template>

<script>
  export default {
    name: "Posts",
    /* assing postsArray import into props
      'props' is a native property of the component */
    props: ["postsArray"]
  }
</script>

<style scoped>

</style>
