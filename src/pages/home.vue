<template>
  <div class="home">
      <Nav />
      <Hero />
      <div class="selectionQuotidienne" id="daily">
          <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1440 320"><path fill="#ffe1e1" fill-opacity="1" d="M0,32L40,80C80,128,160,224,240,250.7C320,277,400,235,480,202.7C560,171,640,149,720,138.7C800,128,880,128,960,133.3C1040,139,1120,149,1200,133.3C1280,117,1360,75,1400,53.3L1440,32L1440,0L1400,0C1360,0,1280,0,1200,0C1120,0,1040,0,960,0C880,0,800,0,720,0C640,0,560,0,480,0C400,0,320,0,240,0C160,0,80,0,40,0L0,0Z"></path></svg>

        <h2 id="pépites">Les pépites culinaires De Bruxelles</h2>
        </div>
        
      <RestaurantRow  v-for="(data, i) in data_restaurant" :key="i" :three_restaurant="data"/>
      <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1440 320"><path fill="#ffc860" fill-opacity="1" d="M0,256L40,234.7C80,213,160,171,240,181.3C320,192,400,256,480,240C560,224,640,128,720,112C800,96,880,160,960,170.7C1040,181,1120,139,1200,144C1280,149,1360,203,1400,229.3L1440,256L1440,0L1400,0C1360,0,1280,0,1200,0C1120,0,1040,0,960,0C880,0,800,0,720,0C640,0,560,0,480,0C400,0,320,0,240,0C160,0,80,0,40,0L0,0Z"></path></svg>
      <About />
  </div>
</template>

<script>
import BDD from "../BDD.js"
import {onMounted, ref} from "vue";

import Hero from "../components/Hero.vue";
import RestaurantRow from "../components/RestaurantRow.vue";
import Nav from "../components/Nav.vue";
import About from "../components/About.vue";

export default {
    name: "Home",
    components : {
        RestaurantRow,
        Hero,
        Nav,
        About
    },
    setup(){
        class Restaurant {
            constructor (name, score, drive_time, href, image){
                this.name = name
                this.score = score
                this.drive_time = drive_time
                this.href = href
                this.image = image
            }
        }

        let data_restaurant = ref([]);

        const makeDataRestaurant = () => {
            let three_restaurant = [];

            for (const restaurant of BDD){

                const new_restaurant = new Restaurant(restaurant.name, restaurant.score, restaurant.drive_time, restaurant.href,restaurant.image)

                if(three_restaurant.length < 3){
                    three_restaurant.push(new_restaurant);
                    data_restaurant.value.push(three_restaurant);
                    three_restaurant = [];
                    console.log(data_restaurant);
                } else{
                    three_restaurant.push(new_restaurant);
                    console.log(three_restaurant);
                }
            }

        }
        onMounted(makeDataRestaurant);
        return {
            data_restaurant
        }
    },

}
</script>

<style>
.selectionQuotidienne{
    background-color: #ffc860;

}
h2{
    margin: 0;
    padding: 0;
}
#pépites{
    color: #870cf7;
    padding: 20px
}
</style>