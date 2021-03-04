<template>
  <div class="favourite-beers">
    <h2>Favourite Beers</h2>
    <favourite-beer-item/>
  </div>
</template>

<script>
import FavouriteBeerItem from './FavouriteBeerItem.vue';

export default {
  components: { 
      'favourite-beer-item' : FavouriteBeerItem 
  },

}
</script>

<style>

</style>