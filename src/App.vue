<template>
  <!--<img alt="Vue logo" src="./assets/logo.png">
  <HelloWorld msg="Welcome to Your Vue.js App"/>-->
  <div id="#app">
  <MyComponents/>
  <!--<my-components />-->
  </div>
</template>

<script>
//import HelloWorld from './components/HelloWorld.vue'
import MyComponents from './components/MyComponents.vue';
export default {
  name: 'App',
  components: {
    //HelloWorld
    MyComponents
  }
}
</script>

<style>

</style>
