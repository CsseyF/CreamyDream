<template>
  <link rel="stylesheet" href="style.css" />

  <div>
    <Popup
      v-if="popupTriggers.buttonTrigger"
      :TogglePopup="() => TogglePopup('buttonTrigger')"
    >
      <h1>{{ Test123 }}</h1>
    </Popup>
  </div>

  <div>
    <img
      id="Logo"
      class="logo"
      alt="Creamy Dream logo"
      src="../assets/donut.png"
      @click="to = '/dashboard'"
    />
    <h2 class="titlefont">Creamy Dream</h2>

    <Cards
      CandyTitle="Donuts"
      path="donuts.jpg"
      Price="8,90"
      @click="Test123 = CandyTitle.value"
    />
    <Cards
      CandyTitle="Chocolate Pancakes"
      path="panquecas-chocolate.jpg"
      Price="15,99"
      @click="() => TogglePopup('buttonTrigger')"
    />
    <Cards
      CandyTitle="Cupcakes"
      path="cupcakes.jpg"
      Price="9,99"
      @click="() => TogglePopup('buttonTrigger')"
    />
    <Cards
      CandyTitle="Fini twister"
      path="fini-twister.jpg"
      Price="5,90"
      @click="() => TogglePopup('buttonTrigger')"
    />
    <Cards
      CandyTitle="Retro Milkshake"
      path="retro-milkshake.jpg"
      Price="11,99"
      @click="() => TogglePopup('buttonTrigger')"
    />
    <Cards
      CandyTitle="Chocolat Ball"
      path="brigadeiros_chocolate.jpg"
      Price="3,79"
      @click="() => TogglePopup('buttonTrigger')"
    />
    <Cards
      CandyTitle="Donuts (No cover)"
      path="donuts-sem-cobertura.jpg"
      Price="6,90"
      @click="() => TogglePopup('buttonTrigger')"
    />
    <Cards
      CandyTitle="Cookies"
      path="cookies.jpg"
      Price="5,99"
      @click="() => TogglePopup('buttonTrigger')"
    />
    <Cards
      CandyTitle="Red Velvet Cake"
      path="red_velvet_cake.jpg"
      Price="48,98"
      @click="() => TogglePopup('buttonTrigger')"
    />
    <Cards
      CandyTitle="Chocotone"
      path="chocotone.jpg"
      Price="10,90"
      @click="() => TogglePopup('buttonTrigger')"
    />
    <Cards
      CandyTitle="Macarrons"
      path="macarrons.jpg"
      Price="4,59"
      @click="() => TogglePopup('buttonTrigger')"
    />
    <Cards
      CandyTitle="Oreo Milka"
      path="oreo_milka.jpg"
      Price="11,90"
      @click="() => TogglePopup('buttonTrigger')"
    />
  </div>
</template>

<script>
import { ref } from "vue";
import Cards from "/src/components/cards/Cards.vue";
import Popup from "/src/components/cards/Popup.vue";

export default {
  name: "Home",
  components: {
    Cards,
    Popup,
  },
  setup() {
    const popupTriggers = ref({
      buttonTrigger: false,
    });

    const TogglePopup = (trigger) => {
      popupTriggers.value[trigger] = !popupTriggers.value[trigger];
    };

    return {
      Popup,
      popupTriggers,
      TogglePopup,
    };
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
