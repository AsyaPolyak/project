<template>
  <!--<img alt="Vue logo" src="./assets/logo.png">
  <HelloWorld msg="Welcome to Your Vue.js App"/>-->
  <div id="#app">
  <MyComponents/>
  <!--<my-components />-->
  <MyLike/>
  <MyPost/>
  </div>
</template>

<script>
//import HelloWorld from './components/HelloWorld.vue'
import MyComponents from './components/MyComponents.vue';
import MyLike from './components/MyLike.vue';
import MyPost from './components/MyPost.vue';
export default {
  name: 'App',
  components: {
    //HelloWorld
    MyComponents,
    MyLike,
    MyPost
  }
}
</script>

<style>

</style>
