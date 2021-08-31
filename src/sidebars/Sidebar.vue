<template>
  <div :class="{'open_sidebar' : isSidebarOpen}" class="sidebar-right">
    <div class="title">
      <ul class="tabMenu">
        <li>Schnellsuche</li>
        <li>Digitalisieren | Persönlich</li>
        <li>Digitalisieren | Öffentlich </li>
        <li>Digitalisieren | Öffentlich (IFM)</li>
        <li>Attributefrage</li>
      </ul>
    </div>
    <div class="p-3">
      <Schnellsuche></Schnellsuche>
    </div>
    <div  class="sidebar-button" @click="openSidebar()">
      <img src="../assets/icons/chevron-left.svg">
    </div>
  </div>
</template>

<script>
import Schnellsuche from '../sites/Schnellsuche.vue' 


export default {
 name : "Sidebarright",
  components: {
    Schnellsuche,
  }, 
data(){
  return {
   isSidebarOpen: false,
  }
}, 
  methods: {
    openSidebar(){
      this.isSidebarOpen = !this.isSidebarOpen;
      console.log("sidebar toggle clicked!")
    }
  } 

}
</script>

<style scoped>
.sidebar-right{
  /* border: 1px solid black; */
  display: block;
  position: absolute;
  right: -41.25em;
  z-index: 2;
  height: 93.5%;
  background-color: #fff;
  width: 41.25em;
  transition: right 1s;
}

.open_sidebar {
  right: 0em;
  transition: right 1s;
}

.title{
  width: 100%;
  height: 3.25rem;
  background-color: #F4F4F4;
  padding: 0.7rem 0;
}

.title p {
  font-size: 1.25em;
  font-weight: 500;
  color: #fff;
}

.tabMenu{
  display: flex;
  flex-direction: row;
  list-style: none;
  /* border: 1px solid green; */
}

.tabMenu li {
  font-size: 0.72em;
  padding: 0.5em 0.65em;
}

.sidebar-button {
  /* border: 1px solid black; */
  position: relative;
  border-radius: 50%;
  background-color: #fff;
  left: -60px; 
  top: calc(100vh / -2);
  width: 2.5em;
  height: 2.5em;
  padding: 0.3em 0.8em;
  cursor: pointer;
}

</style>
