<template>
  <!-- <img alt="Vue logo" src="./assets/logo.png"> -->
  <!-- <HelloWorld msg="Welcome to Your Vue.js App"/> -->
  <MenuList/>
</template>

<script>
// import HelloWorld from './components/HelloWorld.vue'
import MenuList from './components/MenuList.vue'

export default {
  name: 'App',
  components: {
    // HelloWorld,
    MenuList
  }
}
</script>

<style>
body {
    padding: 0;
    margin: 0;
}
</style>
