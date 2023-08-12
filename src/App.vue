<template>
  <AppHeader />
  <hr>
  <AppProducts />
</template>

<script>

import AppHeader from './components/AppHeader.vue'
import AppProducts from './components/AppProducts.vue'

export default {
  name: 'App',
  components: {
    AppHeader,
    AppProducts,
  },
  data() {
    return{

    }
  },
  methods : {
  }

}
</script>

<style src="./scss/app/App.css"></style>

<!-- <template>
  <img alt="Vue logo" src="./assets/logo.png">
  <HelloWorld msg="Welcome to Your Vue.js App"/>
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

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style> -->
