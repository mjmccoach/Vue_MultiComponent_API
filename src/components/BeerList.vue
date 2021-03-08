<template>
  <div class="beer-list">
    <beer-list-item v-for="(beer, index) in beers" :beer="beer" :key="index"></beer-list-item>  
  </div>
</template>

<script>
import BeerListItem from './BeerListItem.vue'


export default {
  components: { 
      'beer-list-item' : BeerListItem 
  },
  props : ['beers']

}
</script>

<style>

</style>