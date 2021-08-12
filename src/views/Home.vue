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

    <Cards CandyTitle="Donuts" path="donuts.jpg" Price="8,90" />
    <Cards
      CandyTitle="Chocolate Pancakes"
      path="panquecas-chocolate.jpg"
      Price="15,99"
    />
    <Cards CandyTitle="Cupcakes" path="cupcakes.jpg" Price="9,99" />
    <Cards CandyTitle="Fini twister" path="fini-twister.jpg" Price="5,90" />
    <Cards
      CandyTitle="Retro Milkshake"
      path="retro-milkshake.jpg"
      Price="11,99"
    />
    <Cards
      CandyTitle="Chocolat Ball"
      path="brigadeiros_chocolate.jpg"
      Price="3,79"
    />
    <Cards
      CandyTitle="Donuts (No cover)"
      path="donuts-sem-cobertura.jpg"
      Price="6,90"
    />
    <Cards CandyTitle="Cookies" path="cookies.jpg" Price="5,99" />
    <Cards
      CandyTitle="Red Velvet Cake"
      path="red_velvet_cake.jpg"
      Price="48,98"
    />
    <Cards CandyTitle="Chocotone" path="chocotone.jpg" Price="10,90" />
    <Cards CandyTitle="Macarrons" path="macarrons.jpg" Price="4,59" />
    <Cards CandyTitle="Oreo Milka" path="oreo_milka.jpg" Price="11,90" />
  </div>

  <div>
    <button>Open Popup</button>

    <Popup v-if="popupTriggers.buttonTrigger">
      <h2>My popup</h2>

    </Popup>

  </div>





</template>

<script>
import { ref } from 'vue';
import Cards from "/src/components/cards/Cards.vue";
import Popup from "/src/components/cards/Popup.vue"

export default {
  name: "Home",
  components: {
    Cards,
    Popup
  },
  setup(){
    const popupTriggers = ref({
      buttonTrigger: false


    })

    return{
      Popup,
      popupTriggers
    }

  }

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
  float: center;
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
