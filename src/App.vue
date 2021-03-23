/* eslint-disable vue/no-unused-components */
<template>
  <div id="app">   
    <navbar/>
    <jumbotron/>
    <container/>
  </div>
</template>

<script>

import navbar from './components/navbar.vue'
import jumbotron from './components/jumbotron.vue'
import container from './components/container.vue'


export default {
  name: 'App',
  components: {
    navbar,
    jumbotron,
    container, 
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

</style>
