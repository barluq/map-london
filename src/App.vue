<script setup lang="ts">
import { Map } from "vue3-openlayers";
import { fromLonLat } from "ol/proj";

</script>

<template>
  <Map.OlMap id="map">
    <Map.OlView :center="fromLonLat([-0.09, 51])" :zoom="9" projection="EPSG:3857" />
    <BasemapTileLayer />
  </Map.OlMap>
</template>

<style scoped>
#map {
  height: 100vh;
}
</style>
