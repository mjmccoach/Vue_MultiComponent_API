<template>
  <div class="beer-list">
    <h1>BeerList here</h1>
    <beer-list-item/>
  </div>
</template>

<script>
import BeerListItem from './BeerListItem.vue'


export default {
  components: { 
      'beer-list-item' : BeerListItem 
  },

}
</script>

<style>

</style>