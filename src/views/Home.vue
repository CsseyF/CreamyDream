<template>
  <link rel="stylesheet" href="style.css" />

  <div>
    <img
      id="Logo"
      class="logo"
      alt="Creamy Dream logo"
      src="../assets/donut.png"
      @click="to = '/dashboard'"
    />
    <h2 class="titlefont">Creamy Dream</h2>

    
    <Cards path='donuts.jpg'/> 
    <Cards path='panquecas-chocolate.jpg'/> 
    <Cards path='donuts-sem-cobertura.jpg'/> 
    <Cards path='cupcakes.jpg'/>
    <Cards path='fini-twister.jpg'/>
    <Cards path='retro-milkshake.jpg'/>
    <Cards path='donuts.jpg'/> 
    <Cards path='panquecas-chocolate.jpg'/> 
    <Cards path='donuts-sem-cobertura.jpg'/> 
    <Cards path='cupcakes.jpg'/>
    <Cards path='fini-twister.jpg'/>
    <Cards path='retro-milkshake.jpg'/>
    <Cards path='donuts.jpg'/> 
    <Cards path='panquecas-chocolate.jpg'/> 
    <Cards path='donuts-sem-cobertura.jpg'/> 
    <Cards path='cupcakes.jpg'/>
    <Cards path='fini-twister.jpg'/>
    <Cards path='retro-milkshake.jpg'/>
    <Cards path='donuts.jpg'/> 
    <Cards path='panquecas-chocolate.jpg'/> 
    <Cards path='donuts-sem-cobertura.jpg'/> 
    <Cards path='cupcakes.jpg'/>
    <Cards path='fini-twister.jpg'/>
    <Cards path='retro-milkshake.jpg'/>
    

  </div>
</template>

<script>
import Cards from "/src/components/cards/Cards.vue";

export default {
  


  name: "Home",
  components: {
    Cards
  },
};
</script>

<style scoped>
.logo {
  
  margin: 0 auto;
  opacity: 0.5;
  text-align: center;
  transition: 0.5s;
  max-width: 100%;
  height: 300px;
  
}

.logo:hover {
  opacity: 1;
  cursor: pointer;
}

@import url("https://fonts.googleapis.com/css2?family=Caveat&display=swap");

.titlefont {
  font-family: "Caveat", cursive;
  font-size: 50px;
  text-align: center;
  margin-top: 0;
  margin-bottom: 3.5em;
  
}

</style>
