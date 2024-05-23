<template>
 <div class="dropdown" :class="[theme, position, transform]">
   <button class="btn toggle-btn" @click="handleDropDown($event)" ref="toggleBtn">
     {{buttonText}} <img :src="icon" alt="icon" v-if="icon">
   </button>
   <ul class="dropdown-menu">
     <li v-for="(each, index) in dropItems" :key="index">
       <a href="javascript:void(0)">{{each}}</a>
     </li>
   </ul>
 </div>
</template>

<script>
export default {
  name: 'DropDown',
  props: ['dropItems', 'theme', 'buttonText', 'icon', 'position', 'transform'],
  data(){
    return {
      isDropDownActive: false
    }
  },
  methods: {
    handleDropDown(e){
      const dropDowns = document.querySelectorAll('.dropdown .dropdown-menu');
      const dropDown = e.target.closest('.dropdown').querySelector('.dropdown-menu');
      // const toggleBtn = e.target.closest('.dropdown').querySelector('.toggleBtn');
      dropDowns.forEach((elem) => {
        if(elem !== dropDown){
          elem.classList.remove('active')
        }else{
          if(elem.classList.contains('active')){
            elem.classList.remove('active')
                e.target.classList.remove('active')
          }else{
            elem.classList.add('active')
            e.target.classList.add('active')
          }
        }
      })
    }
  },

  mounted() {
    console.log(this.theme)
    window.addEventListener('click', (e) => {
      const dropDowns = document.querySelectorAll('.dropdown-menu');
      dropDowns.forEach((elem) => {
        if(!elem.contains(e.target) && !elem.closest('.dropdown').querySelector('.toggle-btn').contains(e.target)){
          elem.classList.remove('active')
          elem.closest('.dropdown').querySelector('.toggle-btn').classList.remove('active');
        }
      })

    })
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
</style>
