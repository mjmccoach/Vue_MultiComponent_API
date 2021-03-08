<template>
  <div id="app">
    <beer-list :beers="beers"/>
    <beer-detail :selectedBeer="selectedBeer"/>
    <favourite-beers :beers="beers"/>
  </div>
</template>

<script>
import { eventBus } from './main.js'
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
      beers : [],
      selectedBeer : null
    }
  },
  mounted() {
    this.getBeers();

    eventBus.$on('beer-selected', beer => (this.selectedBeer = beer));
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
