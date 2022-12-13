<template>
  <div id="app">
    <MyComponents/>
    <MyLike/>
    <MyPost/>
  </div>
</template>

<script>

import MyComponents from './components/MyComponents.vue';
import MyLike from './components/MyLike.vue';
import MyPost from './components/MyPost.vue';
export default {
  name: 'App',
  components: {

    MyComponents,
    MyLike,
    MyPost
  }
}
</script>

<style>

</style>
