<template>
  <div id="app">
    <beer-list :beers="beers"/>
    <beer-detail/>
    <favourite-beers :beers="beers"/>
  </div>
</template>

<script>
import BeerList from './components/BeerList.vue';
import BeerDetail from './components/BeerDetail.vue';
import FavouriteBeers from './components/FavouriteBeers.vue';

export default {
  name: 'App',
  components: {
    'beer-list' : BeerList,
    'beer-detail' : BeerDetail,
    'favourite-beers' : FavouriteBeers
  },
  data() {
    return {
      beers : []
    }
  },
  mounted() {
    this.getBeers()
  },
  methods : {
    getBeers: function() {
      fetch('https://api.punkapi.com/v2/beers')
      .then(res => res.json())
      .then(beers => this.beers = beers)

    }
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
