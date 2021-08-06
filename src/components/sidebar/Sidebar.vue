<script>
import SidebarLink from "./SidebarLink";
import { collapsed, toggleSidebar, sidebarWidth } from "./state";

export default {
  props: {},
  components: { SidebarLink },
  setup() {
    return { collapsed, toggleSidebar, sidebarWidth };
  },
};
</script>

<template>
  <div
    class="sidebar"
    @mouseenter="toggleSidebar"
    @mouseleave="toggleSidebar"
    :style="{ width: sidebarWidth }"
  >
    <SidebarLink to="/" icon="fas fa-home">⠀Home</SidebarLink>
    <br />
    <SidebarLink to="/dashboard" icon="fas fa-utensils">⠀Favorites</SidebarLink>
    <br />
    <SidebarLink to="/analytics" icon="fas fa-fire-alt">⠀Daily specials</SidebarLink>
    <br />
    <SidebarLink to="/friends" icon="fas fa-users">⠀Friends</SidebarLink>
    <br />
    <SidebarLink to="/image" icon="fas fa-cog">⠀Settings</SidebarLink>

  </div>
</template>

<style>
@import url("https://fonts.googleapis.com/css2?family=STIX+Two+Text:ital,wght@1,500&display=swap");

:root {
  --sidebar-bg-color: #ff6961;
  --sidebar-item-hover: #de3a0b;
  --sidebar-item-active: #ffa07a;
}
</style>

<style scoped>


.sidebar {
  color: white;
  background-color: var(--sidebar-bg-color);

  float: left;
  position: fixed;
  z-index: 1;
  top: 0;
  left: 1;
  bottom: 1;
  padding: 0.5em;
  border-radius: 5px;

  transition: 0.3s ease;

  display: flex;
  flex-direction: column;
  font-family: "STIX Two Text", serif;
  

}



.rotate-180 {
  transform: rotate(180deg);
  transition: 0.2s linear;
}


</style>
