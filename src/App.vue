<template>
  <Navbar></Navbar>
  <Sidebarright></Sidebarright>
  <Map></Map>
</template>

<script>
import Navbar from './components/Navbar.vue'
import Map from './components/Map.vue'
import Sidebarright from './sidebars/Sidebar.vue'

export default {
  name: 'App',
  components: {
    Navbar,
    Map,
    Sidebarright
  }
}
</script>

<style>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

html{
  font-size: 16px;
}

#app {
  font-family: Open Sans;
}

body {
  overflow: hidden;
}

.mapboxgl-ctrl-attrib {
  display: none;
}

</style>
