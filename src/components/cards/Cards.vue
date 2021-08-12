<template>
    <div class="box" id = 'card-pic' >

        <img class="card-icons" :src="require(`@/components/cards/photos/${path}`)" alt="Donuts">
        <h2 class="title"> {{CandyTitle}} </h2>
        <br>
        
        <div style="text-align:left">⠀<span class="Pricetitle"> R$:{{Price}} </span> </div> 


    </div>
    


</template>

<script>

export default {
    props: {
       path: String,
       CandyTitle: { required: true , type: String},
       Price: { required: true , type: Number},


    },
    name: "Cards",

}
</script>

<style scoped>

@import url("https://fonts.googleapis.com/css2?family=Caveat&display=swap");

.title{
    font-family: "Caveat", cursive;
    color:darkslategray;
    font-size: 1.8em;
    text-align: center;
    

}

.Pricetitle{
    font-family: "Caveat", cursive;
    color:darkslategray;
    font-size: 1.4em;


}



.card-icons{
    width: 10em;
    height: 10em;
    border-radius: 20%;
    float:left;
    filter: saturate(2.1);
    opacity: 0.8;
    margin: 10px;


}

 .card-icons:hover {
    opacity: 1;
    transform: scale(1.1);
    transition: 0.2s;
    cursor: pointer;
    

} 

.box{
  background-color: #fa807279;
  display: inline-block;
  padding: 15px 15px 20px 15px;
  margin: 20px;
  border-radius: 20%;

}

.box:hover{
    opacity: 1;
    transform: scale(1.1);
    transition: 0.2s;
    cursor: pointer;
    


}





</style>