<template>
  <div>
    <div class="row">
      <p class="col-10">Filter zur Ergebnisliste:</p>
      <img class="col-2" src="../assets/icons/minus-icon.svg" />
    </div>    
    <div class="form-container">
      <form action="">
      <div class="row">
        <div class="col-4">
          <label for="filter">Konzerneigentümer:</label>
          <input type="text" class="form-control" id="inputFilter">
        </div>
        <div class="col-4">
          <label for="filter">Nutzer:</label>
          <input type="text" class="form-control" id="inputFilter">
        </div>
        <div class="col-4">
          <label for="filter">Be-Typ:</label>
          <input type="text" class="form-control" id="inputFilter">
        </div>

      </div>
    </form>
</div> 
  </div>

</template>
<style scoped>

.row p {
  font-size: 0.8125em;
  margin-bottom: 0;
}

.row img {
  width: 0.812em;
  height: 0.812em;
  cursor: pointer;
}

.form-container {
  display: none;
}

.form-control {
  height: 1.5em !important;
  border: 1px solid #222222 !important;
}

label {
  font-size: 0.75em;
}

</style>
