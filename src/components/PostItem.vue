<template lang="html">
  <div class="post">
    <h1 class="title">
      {{ post.title }}
      <button @click="$emit('delete-post', post.id)"
      class="del"> x </button>
    </h1>
    <h3>{{ post.body }}</h3>
  </div>
</template>

<script>
  export default {
    name: "PostItem",
    props: ["post"]
  }
</script>

<style lang="css" scoped>
  .post {
    background: #ffd5d5;
    border-bottom: 1px #fff1e9 solid;
  }

  .title {
    background: #fff1e9;
  }

  .del {
    float: right;
  }
</style>
