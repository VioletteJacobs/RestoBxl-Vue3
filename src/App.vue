<template>
<div id="app">
  <RestaurantCard />
</div>
</template>

<script>
// appeler le composant
import RestaurantCard from './components/RestaurantCard.vue'

export default {
  name: 'App',
  // déclarer les comoposants
  components : {
    RestaurantCard
  }

}
</script>


<style>
@import url('./style/reset.css');
#app {
  
}
</style>
