<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <HelloWorld msg="Hello world"/>
    <TestComponent msg="welcome to the lain"/>
    <!-- bind postsArray to Posts component as a prop -->
    <Posts v-bind:postsArray="postsArray" />
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
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
</style>
