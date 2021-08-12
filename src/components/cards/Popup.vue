<template>
  <main>
    <div class="popup">
      <div class="popup-inner">
        <slot />
        <h1>Hello world</h1>
        <img
          src="./photos/closeicon.png"
          alt="close"
          class="closeicon"
          @click="TogglePopup()"
        />
      </div>
    </div>
  </main>
</template>

<script>
export default {
    props: {
      TogglePopup: String,
      Test123: String 

    }
};
</script>

<style scoped>
.popup {
  position: fixed;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  z-index: 99;
  background-color: rgba(0, 0, 0, 0.2);

  display: flex;
  align-items: center;
  justify-content: center;
}
.popup-inner {
  background: #fff;
  padding: 32px;
  border-radius: 25%;
}
.closeicon {
  width: 20px;
  height: 20px;
  cursor: pointer;
}
</style>
