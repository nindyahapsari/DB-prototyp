<template>
  <div :class="{'open_sidebar' : isSidebarOpen}" class="sidebar-right">
    <div class="title">
      <ul class="nav nav-pills abMenu" id="pills-tab" role="tablist">
        <li class="nav-item">
          <a class="nav-link active" href="#pills-schnellsuche" id="pills-schnellsuche-tab" role="tab" data-toggle="pill" aria-controls="pills-schnellsuche" aria-selected="true">
            Schnellsuche
          </a>        
        </li>
        <li class="nav-item">
          <a class="nav-link" href="#pills-persoenlich" id="pills-persoenlich-tab" role="tab" data-toggle="pill" aria-controls="pills-persoenlich" aria-selected="true">
            Digitalisieren | Persönlich
          </a>
        </li>
        <li>
          <a class="nav-link " href="#pills-oeffentlich" id="pills-oeffentlich-tab" role="tab" data-toggle="pill" aria-controls="pills-oeffentlich" aria-selected="true">
            Digitalisieren | Öffentlich 
          </a>
        </li>
        <li>
          <a class="nav-link " href="#pills-ifm" id="pills-ifm-tab" role="tab" data-toggle="pill" aria-controls="pills-ifm" aria-selected="true">
            Digitalisieren | Öffentlich (IFM)
          </a>
        </li>
        <li>
          <a class="nav-link " href="#pills-attribute" id="pills-attribute-tab" role="tab" data-toggle="pill" aria-controls="pills-attribute" aria-selected="true">
            Attributefrage
          </a>
        </li>
      </ul>

      <div class="tab-content" id="pills-tabContent">
        <div class="tab-pane fade show active p-3" id="pills-schnellsuche" role="tabpanel" aria-labelledby="pills-schnellsuche-tab">
          <Schnellsuche></Schnellsuche>
        </div>
        <div class="tab-pane fade" id="pills-persoenlich" role="tabpanel" aria-labelledby="pills-persoenlich-tab">
          Digitalisieren|Persönlich
        </div>
        <div class="tab-pane fade" id="pills-oeffentlich" role="tabpanel" aria-labelledby="pills-oeffentlich-tab">
          Digi | Öffentlich
        </div>
        <div class="tab-pane fade" id="pills-ifm" role="tabpanel" aria-labelledby="pills-ifm-tab">
          Digi | IFM
        </div>
        <div class="tab-pane fade" id="pills-attribute" role="tabpanel" aria-labelledby="pills-attribute-tab">
          Digi | attribute
        </div>
      </div>
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
  /* padding: 0.5em 0.65em; */
}

.sidebar-button {
  /* border: 1px solid black; */
  position: relative;
  border-radius: 50%;
  background-color: #fff;
  left: -60px; 
  top: calc(100vh / 3);
  width: 2.5em;
  height: 2.5em;
  padding: 0.3em 0.8em;
  cursor: pointer;
}

/* Bootstrap */

.nav-link {
  color: #222222;
  font-size: 0.625em;
  padding: 1em;
  letter-spacing: 0.3px;
}

.nav-pills .nav-link.active {
  color: #D10A10 !important;
  background-color: transparent!important;
  font-weight: 600;

}

</style>
