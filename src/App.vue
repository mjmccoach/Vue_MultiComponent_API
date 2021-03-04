<template>
  <div id="app">
    <beer-list/>
    <beer-detail/>
  </div>
</template>

<script>
import BeerList from './components/BeerList.vue';
import BeerDetail from './components/BeerDetail.vue';

export default {
  name: 'App',
  components: {
    'beer-list' : BeerList,
    'beer-detail' : BeerDetail
    
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
