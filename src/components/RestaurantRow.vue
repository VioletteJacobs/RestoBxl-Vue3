<template>
<div class="restaurantRow">
    <div class="wrapper">
    <RestaurantCard v-for="(card, index) in three_restaurant" :info_restaurant="card" :key="index" /> 

    </div>
</div>
  
</template>

<script>
import RestaurantCard from "./RestaurantCard.vue"
export default {
    name:"restaurantRow",
    components:{
        RestaurantCard
    },
    props : {
        three_restaurant: Array
    }

}
console.log(RestaurantCard);
</script>

<style>
.wrapper{

    background-color:  #ffc860;
}


</style>