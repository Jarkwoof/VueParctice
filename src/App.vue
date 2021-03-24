/* eslint-disable vue/no-unused-components */
<template>
  <div id="app"> 
    <Header/>  
    <ProductList/>
   
  </div>
</template>

<script>


import ProductList from './components/ProductList.vue'
import Header from './components/Header.vue'

export default {
  name: 'App',
  components: {  
    ProductList, 
    Header,
 
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
