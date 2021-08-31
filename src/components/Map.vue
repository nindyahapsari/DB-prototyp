<template>

  <div id="mapcontainer"  class="basemap border"></div>

</template>

<script>
import mapboxgl from 'mapbox-gl';

export default {

  name: "Map",
  data() {
    return {
      accessToken: 'pk.eyJ1IjoibmhhcHNhcmkiLCJhIjoiY2tuOHV2d2Y4MDd0NTJvbXJ3MHg5MjB4YyJ9._wMT0yAmxQ19vOufmjGdNQ'
    };
  },
  mounted() {
    mapboxgl.accessToken = this.accessToken;

    new mapboxgl.Map({
    container: 'mapcontainer',
    style: 'mapbox://styles/mapbox/streets-v11',
    center: [ 7.137962, 50.735051 ],
      zoom: 12,
      maxBounds: [
        [ 6.05, 40.5 ],
        [ 8.248, 80.81 ],
      ],
    });

  }

}

</script>

<style scoped>

.basemap {
  width: 100%;
  min-height: 94vh;
  position: relative;
}

</style>
