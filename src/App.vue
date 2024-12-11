<script setup lang="ts">
import { Map, Layers, Sources } from "vue3-openlayers";

</script>

<template>
    <Map.OlMap id="map">
      <Map.OlView :center="[40, 40]" :zoom="5" projection="EPSG:4326" />
      <Layers.OlTileLayer>
        <Sources.OlSourceOsm />
      </Layers.OlTileLayer>
    </Map.OlMap>
</template>

<style scoped>

#map{
  height: 1000px;
  width: 1000px;
}

</style>
