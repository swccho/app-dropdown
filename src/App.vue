<template>
  <div id="app">
    <div class="grid">
      <div class="card">
        <DropDown :dropItems="dropArr" :buttonText="`Dropdown Toggle`"/>
        <div class="html-content">
          <pre>{{ htmlContent[0] }}</pre>
        </div>
        <div class="desc">
          Here we can pass prop. We can see above code there has two prop.
          <mark>dropItems</mark>
          is an array that contains drop
          down items. And
          <mark>buttonText</mark>
          contains button inner text.
        </div>
      </div>

      <div class="card">
        <DropDown :dropItems="dropArr" :theme="'seabrook'" :buttonText="`Dropdown Toggle`"/>
        <div class="html-content">
          <pre>{{ htmlContent[1] }}</pre>
        </div>
        <div class="desc">
          Here we can see
          <mark>theme</mark>
          prop that contains color of drop down button and drop down menu. Default value is
          <mark>#273c75</mark>.
        </div>
      </div>

      <div class="card">
        <DropDown :dropItems="dropArr" :theme="'periwinkle'" :buttonText="`Dropdown Toggle`"
                  :icon="'/images/down.png'"/>
        <div class="html-content">
          <pre>{{ htmlContent[2] }}</pre>
        </div>
        <div class="desc">
          Here we can see
          <mark>icon</mark>
          prop that contains an image path of drop down button's icon.
        </div>
      </div>

      <div class="card">
        <DropDown :dropItems="dropArr" :theme="'nasturcian'" :position="'right'" :buttonText="`Dropdown Toggle`"
                  :icon="'/images/down.png'"/>
        <div class="html-content">
          <pre>{{ htmlContent[3] }}</pre>
        </div>
        <div class="desc">
          Here we can see
          <mark>position</mark>
          prop that contains position of dropdown-menu whether it's start from left or right. Default value is
          <mark>position</mark>.
        </div>
      </div>

      <div class="card">
        <DropDown :dropItems="dropArr" :theme="'aqua'" :position="'left'" :buttonText="`Dropdown Toggle`"
                  :icon="'/images/down.png'"/>
        <div class="html-content">
          <pre>{{ htmlContent[4] }}</pre>
        </div>
        <div class="desc">
          Here we can see
          <mark>position</mark>
          prop that contains position of dropdown-menu whether it's start from left or right. Default value is
          <mark>left</mark>. <mark>theme</mark>
          prop that contains color of drop down button and drop down menu. <mark>buttonText</mark> prop that
          contains button inner text. <mark>icon</mark>
          prop that contains an image path of drop down button's icon.
        </div>
      </div>

      <div class="card">
        <DropDown :dropItems="dropArr" :theme="'blueberry'" :position="'right'" :buttonText="`Dropdown Toggle`"
                  :icon="'/images/down.png'"/>
        <div class="html-content">
          <pre>{{ htmlContent[5] }}</pre>
        </div>
        <div class="desc">
          Here we can see
          <mark>position</mark>
          prop that contains position of dropdown-menu whether it's start from left or right. Default value is
          <mark>left</mark>. <mark>theme</mark>
          prop that contains color of drop down button and drop down menu. <mark>buttonText</mark> prop that
          contains button inner text. <mark>icon</mark>
          prop that contains an image path of drop down button's icon.
        </div>
      </div>

    </div>
  </div>
</template>

<script>
import DropDown from "@/components/DropDown";

export default {
  name: 'App',
  components: {
    DropDown
  },
  data() {
    return {
      dropArr: [
        'About Us',
        'Service',
        'Pricing',
        'Contact Us',
      ],
      htmlContent: [
        '<DropDown :dropItems="dropArr" :buttonText="`Dropdown Toggle`" />',
        '<DropDown :dropItems="dropArr" :theme="\'seabrook\'" :buttonText="`Dropdown Toggle` :icon="\'/images/down.png\'"/>',
        '<DropDown :dropItems="dropArr" :theme="\'periwinkle\'" :buttonText="`Dropdown Toggle` :icon="\'/images/down.png\'"/>',
        '<DropDown :dropItems="dropArr" :theme="\'nasturcian\'" :position="\'right\'" :buttonText="`Dropdown Toggle` :icon="\'/images/down.png\'"/>',
        '<DropDown :dropItems="dropArr" :theme="\'aqua\'" :position="\'right\'" :buttonText="`Dropdown Toggle` :icon="\'/images/down.png\'"/>',
        '<DropDown :dropItems="dropArr" :theme="\'blueberry\'" :position="\'right\'" :buttonText="`Dropdown Toggle` :icon="\'/images/down.png\'"/>',
      ]
    }
  },
  methods: {},
  mounted() {
  }
}
</script>

<style lang="scss">
@import "assets/scss/style";
</style>
