<template>
  <!-- <img alt="Vue logo" src="./assets/logo.png"> -->
  <!-- <HelloWorld msg="Welcome to Your Vue.js App"/> -->
  <MenuList/>
  <ContentPage/>
</template>

<script>
// import HelloWorld from './components/HelloWorld.vue'
import MenuList from './components/MenuList.vue'
import ContentPage from './components/ContentPage.vue'

export default {
  name: 'App',
  components: {
    // HelloWorld,
    MenuList,
    ContentPage
  }
}
</script>

<style>
body {
    padding: 0;
    margin: 0;
}
</style>
