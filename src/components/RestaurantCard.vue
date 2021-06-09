<template>
   <div class="restaurant_card">
       
       <div class="restaurant_image">
       </div>
       <div class="restaurant_info">
           <div class="title">
               <p class="name">{{info_restaurant.name}}</p>
               <P class="score"> {{info_restaurant.score}}</P>
           </div>
           <p class="time"> Temps d'attente : {{info_restaurant.drive_time}}</p>
       </div>
   </div>
</template>

<script>
export default {
    name:"restaurantCard",
    props:{
        info_restaurant : Object
    },
    setup(props){
        console.log(props.info_restaurant);
    }
}
</script>

<style>
.restaurant_card{
    width: 32%;
    height: 60vh;
}
.restaurant_image{
    height: 70%;
    background-image: url("../../public/images/resto_un.jpeg");
    background-position: center;
    background-size: center;

}
.title{
    display: flex;
    align-items: center;
    justify-content: space-between;
}
.name{
    font-size: 1.5rem;
    margin: 1px;
    color: #03224C
}
.score{
    display: flex;;
    height: 25px;
    width: 30px;
    align-items: center;
    font-size: 0.8rem;
    background-color: #870cf7 ;
    color: white;
    border-radius: 50px;
    padding: 6px;
    margin-top: 10px;
    justify-content: center;
    align-items: center;
    }
.time{
    margin: 0
}
</style>