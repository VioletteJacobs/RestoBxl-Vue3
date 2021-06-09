<template>
<nav>
  <ul>
      <li> <a href="/#daily">Sélection quotidienne</a> </li>
      <li> <a href="/#about">About</a> </li>
      <li><a href="/#contact">contact</a> </li>
  </ul>

</nav>
</template>

<script>
export default {

}
</script>

<style>
nav{
    background-color: #ffe1e1;
    -webkit-backdrop-filter: blur(2px);
    backdrop-filter: blur(2px);
    padding-top: 20px;
    
}
ul{
    list-style: none;
    display: flex;
    justify-content: space-around;
    margin: 0;
    padding-top: 20px
}
li{
    color: #ffc860;
    font-size: 25px

}

</style>