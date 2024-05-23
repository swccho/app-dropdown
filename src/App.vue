<template>
  <div id="app">
    <HelloWorld msg="Welcome to Your Vue.js App"/>
    <div class="dropdown">
      <button class="btn btn-secondary toggle-btn" @click="toggleDropDown">
        Dropdown button
      </button>
      <DropDown :dropItems="dropArr" ref="dropDown" />
    </div>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue';
import DropDown from "@/components/DropDown";

export default {
  name: 'App',
  components: {
    HelloWorld,
    DropDown
  },
  data () {
    return {
      dropArr: [
          'About Us',
          'Service',
          'Pricing',
          'Contact Us',
      ],
      isDropDownActive: false
    }
  },
  methods: {
    toggleDropDown(){
      this.$refs.dropDown.handleDropDown()
    }
  }
}
</script>

<style lang="scss">
@import "assets/scss/style";
</style>
