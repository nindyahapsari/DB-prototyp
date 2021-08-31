<template>
  <div>
    <Schnellfilter></Schnellfilter>
    <hr>
    <div> Here is the other filter</div>
    <hr>
    <div class="wrapper">
      <div class="container">
        <div class="row">
          <div class="col-6 d-flex flex-row">
            <span>O</span>
            <p>Gemerkt: 15</p>
          </div>
          <div class="col-6 d-flex justify-content-end parent">
            <div class="checkbox-container mx-2">
              <input class="checkbox" type="checkbox" value="" id="defaultCheck1">
            </div>
            <div class="dropdown">
              <button class="button-table dropdown-toggle"
                      type="button" id="dropdownMenu1" data-toggle="dropdown">
               Als PDF 
              </button>
              <div class="dropdown-menu" aria-labelledby="dropdownMenu1">
                <a class="dropdown-item" href="#!">Action</a>
                <a class="dropdown-item" href="#!">Another action</a>
              </div>
            </div>
          </div>
          <Table></Table>
        </div>
      </div>
    </div>
  </div>

</template>
<script>
import Table from '../components/Table.vue';
import Schnellfilter from '../components/SchnellsucheFilter.vue';

export default {

  name: "Schnellsuche",
  components: {
    Table, 
    Schnellfilter,
  },
}


</script>
<style scoped>

.form-control {
  height: 1.5em !important;
  border: 1px solid #222222 !important;
}

.wrapper {
  display: flex;
  flex-direction: column;
  overflow: hidden;
}

.checkbox-container input {
  height: 1.75em !important;
  /* width: 1.7rem !important; */
  border: 1px solid red;
}

.button-table {
  width: 8.3em;
  height: 1.7em;
  padding: 0.1em 0.7em;
  border: 1px solid #222222;
  border-radius: 5px;
  font-size: 0.8em;
  background-color: #ffffff;

}



</style>
