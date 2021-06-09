<template>
<div id="app">
  <Home />
</div>
</template>

<script>
// appeler le composant
import Home from './pages/home.vue'

export default {
  name: 'App',
  // déclarer les composants
  components : {
    Home
  }

}
</script>


<style>
@import url('./style/reset.css');
#app {
  font-family: 'Lucida Sans', 'Lucida Sans Regular', 'Lucida Grande', 'Lucida Sans Unicode', Geneva, Verdana, sans-serif;
    background-color: #ffe1e1;
    padding: 0;
    position: relative
}
</style>
