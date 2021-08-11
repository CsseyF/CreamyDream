<template>
    <div class="box" id = 'card-pic' >
        <img class="card-icons" :src="require(`@/components/cards/photos/${path}`)" alt="Donuts">
        
    </div>

</template>

<script>
export default {
    props: {
       path: String
    },
    name: "Cards",

}
</script>

<style scoped>

.card-icons{
    width: 10em;
    height: 10em;
    border-radius: 20%;
    float:left;
    filter: saturate(2.1);
    opacity: 0.8;


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
  padding: 15px 15px 90px 15px;
  margin: 20px;
  text-align: center;
  border-radius: 20%;

}

.box:hover{
     opacity: 1;
    transform: scale(1.1);
    transition: 0.2s;
    cursor: pointer;
    


}



</style>