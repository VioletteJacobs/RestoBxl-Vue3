<template>
   <div class="restaurant_card">
       <h2>Les meilleures restaurants De Bruxelles</h2>
       <div class="restaurant_image">
       </div>
       <div class="restaurant_info">
           <div class="title">
               <p class="name">Racines</p>
               <P class="score"> 4.9/5</P>
           </div>
           <p class="time"> 45 - 55min</p>
       </div>
   </div>
</template>

<script>
export default {

}
</script>

<style>
.restaurant_card{
    width: 32%;
    height: 30vh;
}
.restaurant_image{
    height: 70%;
    background-image: url("../../public/images/resto_un.jpeg");
    background-size: cover;
    background-size: center;

}
.title{
    display: flex;
    align-items: center;
    justify-content: space-between;
}
.name{
    font-size: 1.5rem;
    margin: 1px
}
.score{
    height: 25px;
    width: 30px;
    align-items: center;
    font-size: 0.8rem;
    background-color: #AAF0D1 ;
    border-radius: 50%;
    padding-top: 6px;
    padding-right: 1px;
    padding-left : 3px;
    margin: 1px
    }
.time{
    margin: 0
}
</style>