<template>
<div class="hero">
    <div class="slogan">
        <h1>C'est fini de rester à la maison, <br> profitons de l'été au <span id="resto_slogan"> Restaurant</span> !</h1>
        <span class="description">Après des mois de pizzas réchauffées, de banana bread et de chips devant Netflix, nous avons enfin l'occasion de retourner dans nos restaurant préférés. Voici une petite sélection Bruxelloise pour vous inspirer si vous les avez oublié.</span>

        <button id="btn_daily"> <a href="/#daily" id="herf_hero">Un resto au top ?!</a> </button>

    </div>
    <div class="hero_image">
        <img src="../../public/images/hero.png" alt="illustration deux personnes se retrouvant pour aller au restaurant" id="image_slogan">
    </div>

</div>
</template>

<script>
export default {

}
</script>

<style>
.hero{
    display: flex;
    justify-content: space-evenly;
    padding: 50px;
    height: 100vh;
    padding-bottom: 0;
    margin-bottom: 0;
}
.slogan{
    padding: 20px;
    display: flex;
    flex-direction: column;
}
h1{
    color: #870cf7;
    font-size: 60px;
    padding: 20px;
    font-family: Cambria, Cochin, Georgia, Times, 'Times New Roman', serif;
    text-transform:uppercase;

}
#resto_slogan{
    color: #ffc860
}
.description{
    color: #293133
}
.hero_image{
    top: 50px;
    height: 60vh;
}
#image_slogan{
    
    height: 70vh;
    width: 500px
}
#btn_daily{
    margin-top : 100px;
    background-color: #ffc860;
    color: black;
    border-radius: 50px;
    padding: 18px;
    border: none;
    justify-content: center;
}
#href_hero{
    text-decoration: none;

}
</style>