<template>
  <ul :class="{'dropdown-menu': true, 'active': isDropDownActive}">
    <li v-for="(each, index) in dropItems" :key="index">
      <a href="">{{each}}</a>
    </li>
  </ul>
</template>

<script>
export default {
  name: 'HelloWorld',
  props: ['msg', 'dropItems'],
  data(){
    return {
      isDropDownActive: false
    }
  },
  methods: {
    handleDropDown(){
      this.isDropDownActive = !this.isDropDownActive
    }
  },

  mounted() {
    window.addEventListener('click', (e) => {
      const toggleButton = document.querySelector('.dropdown .toggle-btn');
      const dropDown = document.querySelector('.dropdown-menu');
      if(!dropDown.contains(e.target) && !toggleButton.contains(e.target)){
        this.isDropDownActive = false;
      }
    })
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
</style>
