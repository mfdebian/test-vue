<template>
  <div id="app">
    <h1 class="title">Welcome</h1>
    <HelloWorld msg="Hello world"/>
    <TestComponent msg="welcome to the lain"/>
    <!-- bind postsArray to Posts component as a prop -->
    <Posts v-bind:postsArray="postsArray" v-on:delete-post="deletePost" />
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import TestComponent from './components/TestComponent.vue'
import Posts from './components/Posts.vue'

export default {
  name: 'app',
  components: {
    HelloWorld,
    TestComponent,
    Posts
  },
  // data() is a vue native function _apparently_
  data() {
    return {
      postsArray: [
        {
          id: 0,
          title: 'math',
          body: 'exponential functions',
          tags: ['math', 'functions', 'exponential']
        },
        {
          id: 1,
          title: 'comunications',
          body: 'political facts',
          tags: ['comunications', 'facts', 'politics']

        },
        {
          id: 2,
          title: 'music',
          body: 'flac download',
          tags: ['music', 'flac', 'download']
        }
      ]
    }
  },

  methods: {
    deletePost(postid) {
      this.postsArray = this.postsArray.filter(post => post.id !== postid);
    }
  }
}
</script>

<style>
    @import url('https://fonts.googleapis.com/css?family=Roboto&display=swap');

    body, html {
    min-height: 100%;
    background: #45454d;
    margin: 5px;
    overflow-y: hidden;
  }
  #app {
    font-family: 'Roboto', sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-align: center;
    color: #2c3e50;
  }
  .title {
    background: #ff4893;
  }

</style>
