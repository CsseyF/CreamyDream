<script>
import Sidebar from "@/components/sidebar/Sidebar";
import {sidebarWidth} from "@/components/sidebar/state";


export default {
  components: { Sidebar, },
  setup() {
    return { sidebarWidth }
  },



};
</script>

<template >
  
  <Sidebar />
    <div>
      <router-view />
    </div>

</template>


<style>
:root{
  background-color: rgba(255, 160, 122,0.4);
  
}
</style>




<style>
#app {
  text-align: center;
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
}

#nav {
  padding: 30px;
}

#nav a {
  font-weight: bold;
  color: #2c3e50;
}

#nav a.router-link-exact-active {
  color: #42b983;
}

</style>
