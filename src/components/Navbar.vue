<template>
<nav class="nav-container">
  <a class="logo-container" href="">
    <img class="logo"  src="../assets/DB_logo_red_200px_rgb.png" alt="Deutschebahn logo">
    <div class="text-logo-container d-flex flex-column">
      <p class="logo-text">DB Imm Maps - Flächeninformation DBImm</p>
      <p class="logo-small-text">Version 3.12</p>
    </div>
  </a>
  <div class="icons-container">  
    <li class="nav-icon" ><img src="../assets/icons/layer.svg" alt=""></li>
    <li class="nav-icon" ><img src="../assets/icons/legend.svg" alt=""></li>
    <li class="nav-icon" ><img src="../assets/icons/info.svg" alt=""></li>
    <li class="nav-icon" ><img src="../assets/icons/printer.svg" alt=""></li>
    <li class="nav-icon" ><img src="../assets/icons/ruler.svg" alt=""></li>
    <li class="nav-icon" ><img src="../assets/icons/layer_2.svg" alt=""></li>
    <li class="nav-icon" ><img src="../assets/icons/globe.svg" alt=""></li>
    <li class="nav-icon" ><img src="../assets/icons/export.svg" alt=""></li>
    <li class="ham-icon"  @click="hamToggle()" ><img src="../assets/icons/ham-menu.svg" alt="">
      <Dropdown :class="{'navDropdown' : showDropdown}" ></Dropdown>
    </li>
  </div>

</nav>
</template>

<script>
import Dropdown from './dropdown.vue'

export default {
 name : 'Navbar',
 components: {
    Dropdown,
  }, 
 data() {
   return {
      showDropdown: false,
   }
  }, 
  methods: {
    hamToggle(){
      this.showDropdown = !this.showDropdown;
    }
  }, 
}

</script>


<style scoped>

.nav-container{
  display: flex;
  flex-direction: row;
  padding: 0  0.5em;
  /* padding: 1.663rem 1rem 0 1rem; */
}

.logo-container{
  width: 33.125em;
  margin: 0.5em  0;
  display: flex;
  flex-direction: row;
  justify-content: center;
  align-items: center;
  /* height: 2.75em; */

}

.logo{
  width: 3.938em;
  height: 2.75em;
}

.text-logo-container {
  margin: 0 0.3rem;
}

.logo-text{
  font-size: 1.25em;
  font-weight: 600;
  color: #222222;
  margin: 0;
}

.logo-small-text {
  font-size: 0.9375em;
  list-style: none;
  color: #222222;
  margin: 0;
}

.icons-container{
  margin-left: 35rem;
  display: flex;
  align-items: center;
  list-style: none;
}

.nav-icon{
  margin-right: 3.138em;
}

.nav-icon img {
  width: 1.5em;
}

.ham-icon{
  margin-left: 10em;
}

.navDropdown {
  display: block; 
  width: 12.3rem;
  display: flex;
  flex-direction: column;
  padding: 0.5em 1.5em;

}

</style>
