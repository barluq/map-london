<script setup lang="ts">
import { Map, Layers, Sources } from "vue3-openlayers";
import { Maptiler } from "./utils/basemaps";
import { fromLonLat } from "ol/proj";

</script>

<template>
  <Map.OlMap id="map">
    <Map.OlView :center="fromLonLat([-0.09, 51])" :zoom="9" projection="EPSG:3857" />
    <Layers.OlTileLayer>
      <Sources.OlSourceXyz :url="Maptiler.DarkDataviz" :tileSize="[512, 512]" />
    </Layers.OlTileLayer>
  </Map.OlMap>
</template>

<style scoped>
#map {
  height: 100vh;
}
</style>
