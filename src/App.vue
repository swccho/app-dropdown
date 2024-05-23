<template>
  <div id="app">
    <HelloWorld msg="Welcome to Your Vue.js App"/>
    <div class=""></div>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'

export default {
  name: 'App',
  components: {
    HelloWorld
  }
}
</script>

<style lang="scss">
@import "assets/scss/style";
</style>
