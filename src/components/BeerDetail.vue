<template>
  <div class='beer-detail'>
    <h4> {{ selectedBeer.name }} </h4>
    <p> {{ selectedBeer.abv }}</p>
    <p> {{ selectedBeer.description }} </p>
  </div>
</template>

<script>
export default {
    props : ['selectedBeer']

}
</script>

<style>

</style>