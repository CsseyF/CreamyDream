<template>
  <div class="home">
    <img
      id="Logo"
      class="logo"
      alt="Creamy Dream logo"
      src="../assets/donut.png"
      @click="to = '/dashboard'"
    />
    <h2 class="titlefont">Creamy Dream</h2>
    <HelloWorld msg="Welcome to Your Vue.js App" />
  </div>
</template>

<script>
export default {
  name: "Home",
  components: {},
};
</script>

<style>
.logo {
  text-align: center;
  opacity: 0.5;
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
}
</style>
