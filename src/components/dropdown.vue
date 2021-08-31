<template>
  <div class="drop-down">
    <a href="">Druck "NovSächStrG"</a>
    <a href="">Leitungauskunft</a>
    <a href="">Hilfe</a>
    <a href="">Neu Laden</a>
    <a href="">KML</a>
    <a href="">IVL</a>
    <a href="">Koordinaten</a>
    <a href="">BCM DB Immobillien</a>
    <a href="">Ansicht Bearbeiten</a>
    <a href="">Ansicht Laden</a>
  </div>

</template>

<script>

export default {
 name : 'Dropdown' 
} 

</script>


<style scoped>
.drop-down{
  /* border: 1px solid black; */
  /* display: block; */
  position: absolute;
  z-index: 10;
  right: 0;
  top: 3.7em;
  background-color: #fff;
  width: 12.3rem;
  display: flex;
  flex-direction: column;
  padding: 0.5em 1.5em;
  display: none;
}

.drop-down  > a {
  margin: 0.5em 0;
  font-size: 0.813em;
  font-weight: 600;
  color: #222222;
}

</style>
