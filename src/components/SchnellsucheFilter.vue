<template>
  <div>
    <form>
      <div class="row form-group">
        <div class="col-8">
          <label for="filter">Filter:</label>
          <input type="text" class="form-control" id="inputFilter">
        </div>
        <div class="col-4 d-flex align-self-end justify-content-end">
          <button class=" filterBtn">Btn</button>
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
            <input type="text" class="form-control col-5 mx-1" id="inputFlurstueck">
            <p> / </p>
            <input type="text" class="form-control col-5 mx-1" id="inputFlurstueck">
          </div>
        </div>
      </div>
      <div class="d-flex justify-content-end">
        <button type="submit" class="btn btn-outline-secondary mx-2">Suchen</button>
        <button type="submit" class="btn btn-outline-secondary mx-2">Reset</button>
      </div>
    </form>
  </div>
</template>
