<script setup lang="ts">
import { Map, Layers, Sources } from "vue3-openlayers";
import { Maptiler } from "./utils/sourcesMap";

</script>

<template>
  <Map.OlMap id="map">
    <Map.OlView :center="[40, 40]" :zoom="10" projection="EPSG:3857" />
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
