<script setup lang="ts">
import L from 'leaflet';
import 'leaflet/dist/leaflet.css';
import { ref, onMounted } from 'vue'


onMounted(() => {
  const map = L.map('map').setView([51.505, -0.09], 13); // Set map center and zoom level

  // Add a tile layer (this example uses OpenStreetMap)
  L.tileLayer('https://{s}.tile.openstreetmap.org/{z}/{x}/{y}.png', {
    attribution: '&copy; <a href="https://www.openstreetmap.org/copyright">OpenStreetMap</a> contributors'
  }).addTo(map);

})

</script>

<template>
  <aside>
    <div id="map"></div>
  </aside>
</template>

<style scoped>
#map {
  height: 100vh;
  width: 100vw;
}
</style>
