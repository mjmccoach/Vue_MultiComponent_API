<template>
  <p v-on:click="handleSelectBeer"> {{ beer.name }} </p>
</template>

<script>
import { eventBus } from '../main.js'

export default {
    props: ['beer'],
    methods : {

    handleSelectBeer: function() {
      eventBus.$emit('beer-selected', this.beer)
    }
    }

}
</script>

<style>

</style>