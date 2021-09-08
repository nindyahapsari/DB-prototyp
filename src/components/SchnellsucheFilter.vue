<template>
  <div>
    <form>
      <div class="row form-group">
        <div class="col-8">
          <label for="filter">Filter:</label>
          <input type="text" class="form-control" id="inputFilter">
        </div>
        <div class="col-4 d-flex align-self-end justify-content-end">
          <button class=" filterBtn">
            <img class="pencil-icon" src="../assets/icons/pencil_white.svg">
          </button>
        </div>
      </div>
      <div class="row form-group">
        <div class="col-6">
          <label for="gemarkungNr">Gemarkung-Nr:</label>
          <input type="text" class="form-control" id="inputGemarkungNr">
        </div>
        <div class="col-6">
          <label for="gemarkungName">Gemarkung-Name:</label>
          <input type="text" class="form-control" id="inputGemarkungName">
        </div>
      </div>
      <div class="row form-group">
        <div class="col-6">
          <label for="flur">Flur:</label>
          <input type="text" class="form-control" id="flur">
        </div>
        <div class="col-6">
          <label for="gemarkungnr">Flurstück:</label>
          <div class="row px-2">
            <input type="text" class="form-control col-5 mx-2" id="inputFlurstueck">
            <p> / </p>
            <input type="text" class="form-control col-5 mx-2" id="inputFlurstueck">
          </div>
        </div>
      </div>
      <div class="d-flex justify-content-end">
        <button type="submit" class="normalbtn">
          <p>Suchen</p>
        </button>
        <button type="submit" class="normalbtn">
          <p>Reset</p>
        </button>
      </div>
    </form>
  </div>
</template>

<style scoped>


.filterBtn {
  width: 1.9375em;
  height: 1.5em;
  background-color: #D10A10;
  border: none;
  border-radius: 4px;
}

.pencil-icon {
  width: 16px;
  height: 16px;
  margin-bottom: 2px;
}

.normalbtn {
  width: 8.625em;
  height: 2.375em;
  background-color: #CECECE;
  border-radius: 4px;
  border: none;
  color: #222222;
  margin: 0 0.3em;
}

.normalbtn p {
  font-size: 0.75em;
  margin: 0.3em auto;
  font-weight: 500;
}

.form-control {
  height: 1.5em !important;
  border: 1px solid #222222 !important;
}

label {
  font-size: 0.75em;
}
</style>
